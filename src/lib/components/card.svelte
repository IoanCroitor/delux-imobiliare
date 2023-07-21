<script lang="ts">
    // export let title:string;
    export let isRentable=true;
    export let isAdFavourite=false;
    
    
</script>

<div class="w-[90vw] sm:w-96 md:w-80 2xl:w-72 rounded-2xl overflow-hidden backdrop-blur-2xl bg-gray-900">
    <div class="relative w-full h-44">
        <img
        class="w-full h-full object-cover object-center rounded-2xl user-select-none pointer-events-none"
        src="https://images.unsplash.com/photo-1606402179428-a57976d71fa4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NHx8aG91c2UlMjBuaWdodHxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=600&q=60"
        alt="casa"/>

        <div class="absolute top-2 left-2 flex items-center justify-center align-middle w-auto h-8 px-2 bg-black/20 hover:bg-black/40 transition duration-150 ease-linear rounded-full backdrop-blur-3xl"> 
            <p class="text-white font-bold">100</p>
            <p class="text-white font-bold">€</p>
            {#if isRentable}
            <p class="text-white font-thin">/luna</p>
            {/if}
        </div>

        <button class="absolute top-2 right-2 flex items-center justify-center align-middle w-8 h-8  bg-black/20 hover:bg-black/40 rounded-full backdrop-blur-3xl transition duration-150 ease-linear"
        on:click={()=>isAdFavourite = !isAdFavourite}>
            <svg class={`w-5 h-5 transition duration-100 ease-linear stroke-2 ${isAdFavourite ? 'stroke-red-500 scale-110 fill-red-500' : 'stroke-white fill-none'}`}
            viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
                <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                <path d="M19.5 12.572l-7.5 7.428l-7.5 -7.428a5 5 0 1 1 7.5 -6.566a5 5 0 1 1 7.5 6.572" />
            </svg>
        </button>

    </div>

    <!-- bg-gray-800 rounded-xl -->
    <div class="m-1">
        <div class="flex flex-row pt-1 px-2 justify-between items-center">
            <p class="text-gray-200 text-md font-bold">Vila Duplex</p>
            {#if isRentable}
                <div class="px-1 flex flex-row items-center bg-blue-500 rounded-full h-min">
                    <p class="pr-[1px] text-gray-100 text-sm font-bold">2.0</p>
                    <svg class="w-4 h-4 fill-gray-100" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
                        <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                        <path d="M8.243 7.34l-6.38 .925l-.113 .023a1 1 0 0 0 -.44 1.684l4.622 4.499l-1.09 6.355l-.013 .11a1 1 0 0 0 1.464 .944l5.706 -3l5.693 3l.1 .046a1 1 0 0 0 1.352 -1.1l-1.091 -6.355l4.624 -4.5l.078 -.085a1 1 0 0 0 -.633 -1.62l-6.38 -.926l-2.852 -5.78a1 1 0 0 0 -1.794 0l-2.853 5.78z" stroke-width="0"/>
                    </svg>
                </div>
            {/if}
        </div>

        <div class=" pb-1 pl-2 flex flex-row items-center">
            <svg class="w-3 h-3 stroke-gray-400 stroke-2 fill-none" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
                <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                <path d="M21 3l-6.5 18a.55 .55 0 0 1 -1 0l-3.5 -7l-7 -3.5a.55 .55 0 0 1 0 -1l18 -6.5" />
            </svg>            
            <p class=" text-gray-400 text-xs font-medium">Strada Principala nr. 521 Babeni</p>
        </div>

        <div class="px-2 py-1 flex flex-row justify-evenly">

            <div class="flex row items-center bg-gray-800 rounded-full py-1 px-2">
                <svg class="w-4 h-4 stroke-1 fill-gray-100" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
                    <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                    <path d="M3 6a1 1 0 0 1 .993 .883l.007 .117v6h6v-5a1 1 0 0 1 .883 -.993l.117 -.007h8a3 3 0 0 1 2.995 2.824l.005 .176v8a1 1 0 0 1 -1.993 .117l-.007 -.117v-3h-16v3a1 1 0 0 1 -1.993 .117l-.007 -.117v-11a1 1 0 0 1 1 -1z" stroke-width="0"/>
                    <path d="M7 8a2 2 0 1 1 -1.995 2.15l-.005 -.15l.005 -.15a2 2 0 0 1 1.995 -1.85z" stroke-width="0"/>
                </svg>
                <p class="text-gray-100 text-sm pl-1 font-medium">4</p>
            </div>

            <div class="flex row items-center bg-gray-800 rounded-full py-1 px-2">
                <svg class="w-4 h-4 stroke-1 fill-gray-100" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
                    <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                    <path d="M11 2a1 1 0 0 1 .993 .883l.007 .117v2.25a1 1 0 0 1 -1.993 .117l-.007 -.117v-1.25h-2a1 1 0 0 0 -.993 .883l-.007 .117v6h13a2 2 0 0 1 1.995 1.85l.005 .15v3c0 1.475 -.638 2.8 -1.654 3.715l.486 .73a1 1 0 0 1 -1.594 1.203l-.07 -.093l-.55 -.823a4.98 4.98 0 0 1 -1.337 .26l-.281 .008h-10a4.994 4.994 0 0 1 -1.619 -.268l-.549 .823a1 1 0 0 1 -1.723 -1.009l.059 -.1l.486 -.73a4.987 4.987 0 0 1 -1.647 -3.457l-.007 -.259v-3a2 2 0 0 1 1.85 -1.995l.15 -.005h1v-6a3 3 0 0 1 2.824 -2.995l.176 -.005h3z" stroke-width="0"/>
                </svg>
                <p class="text-gray-100 text-sm pl-1 font-medium">4</p>
            </div>

            <div class="flex row items-center bg-gray-800 rounded-full py-1 px-2">
                <svg class="w-4 h-4 stroke-2 stroke-gray-100" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
                    <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                    <path d="M8 18a2 2 0 1 0 -4 0a2 2 0 0 0 4 0z" />
                    <path d="M20 18a2 2 0 1 0 -4 0a2 2 0 0 0 4 0z" />
                    <path d="M20 6a2 2 0 1 0 -4 0a2 2 0 0 0 4 0z" />
                    <path d="M8 6a2 2 0 1 0 -4 0a2 2 0 0 0 4 0z" />
                    <path d="M6 8v8" />
                    <path d="M18 16v-8" />
                    <path d="M8 6h8" />
                    <path d="M16 18h-8" />
                </svg>
                <p class="text-gray-100 text-sm pl-1 font-medium">380 mp</p>
            </div>

            <div class="flex row items-center bg-gray-800 rounded-2xl p-1">
                <p class="text-gray-100 text-sm font-semibold">+9</p>
            </div>
        </div>
        

    </div>
</div>
