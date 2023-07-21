<script lang="ts">
    type currencyType = '€' | 'lei';
    export let priceEur:number= 120000;
    export let priceEurRent:number=600;
    let conversionRate = 4.67;
    let AdPrice = priceEur;
    let AdPriceRent = priceEurRent;
    let currency:currencyType= "€", currencyRent:currencyType= "€";

    //I dont know how to this in one single function Cleanly?
    function priceConversion(price:number){
        currency = currency === '€' ? 'lei' : '€';

        if(price===priceEur)
            return price * conversionRate;
        else
            return priceEur;
    }

    function priceConversionRent(price:number){
        currencyRent = currencyRent === '€' ? 'lei' : '€';

        if(AdPriceRent===priceEurRent)
            return price * conversionRate;
        else
            return priceEurRent;
    }

</script>
<div class="relative flex flex-row items-center">
    <button on:click={()=>AdPrice = priceConversion(AdPrice)}>
        <p class="text-2xl text-gray-50 font-semibold">{AdPrice}<span class="font-extralight">{currency}</span></p>
    </button>
    <svg class="w-6 h-6 fill-fuchsia-300" viewBox="0 0 24 24">
        <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
        <path d="M12 7a5 5 0 1 1 -4.995 5.217l-.005 -.217l.005 -.217a5 5 0 0 1 4.995 -4.783z" />
    </svg>
    <button on:click={()=>AdPriceRent = priceConversionRent(AdPriceRent)}>
        <p class="text-2xl text-gray-100 font-semibold">{AdPriceRent}<span class="font-extralight">{currencyRent}</span><span class="font-thin">/luna</span></p>
    </button>
</div>