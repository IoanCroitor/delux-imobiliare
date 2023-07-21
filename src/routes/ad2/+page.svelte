<script>
    import ImageGrid from "./imageGrid.svelte";
    import Rating from "./rating.svelte";
    import Price from "./price.svelte";
</script>

<div class="relative mt-20 max-w-7xl mx-auto">
    <div class="flex flex-col px-2">

        <div class="w-full">
            <ImageGrid />
        </div>

        <div class="w-full xl:w-4/6 xl:pr-2 px-2 xl:px-0">

            <div class="flex flex-row justify-between py-2 flex-wrap">
                <div class="shadow-inner shadow-gray-800 px-2 rounded-full">
                    <Price/>
                </div>
                <div class="h-min shadow-inner shadow-gray-800 px-2 rounded-full">
                    <Rating/>
                </div>
            </div>
            
            <div class="flex flex-col">
                <h1 class="text-2xl md:text-4xl xl:text-4xl text-gray-200 font-semibold tracking-tight">Modern Home with Spectacular Views</h1>
                <p class=" text-gray-400 text-md md:text-xl font-extralight">
                    Strada Maceselor, nr.180, Rm. Valcea
                    <span class="text-gray-500 text-md md:text-xl font-extralight">VL</span>
                </p>
            </div>
            
            <div class="grid grid-flow-col gap-2 justify-between ">
                <div class="w-12 h-12 bg-gray-50"></div>
                <div class="w-12 h-12 bg-gray-50"></div>
                <div class="w-12 h-12 bg-gray-50"></div>
                <div class="w-12 h-12 bg-gray-50"></div>
                <div class="w-12 h-12 bg-gray-50"></div>

            </div>
        </div>
    </div>
</div>