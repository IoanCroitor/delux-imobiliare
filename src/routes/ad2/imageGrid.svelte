
<script>
  import { onMount } from 'svelte';
  import Contact from './contact.svelte';
  import {
    Accordion,
    AccordionContent,
    AccordionItem,
    AccordionTrigger
  } from "$components/ui/accordion";
    
  // Assuming you have an array of product images
  let productImages = [
    'https://images.livspace-cdn.com/plain/https://jumanji.livspace-cdn.com/magazine/wp-content/uploads/sites/2/2021/08/18133115/cover-15-1.png',
    'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQQDQqVQLBIy0X8Yw-HE8DXK2tDho9EEheUOaiL2a4K&s',
    'https://hips.hearstapps.com/hmg-prod/images/martha-mulholland-standard-architecture-malibu-house-094-edit-1647617137.jpg?crop=1.00xw:0.752xh;0,0.163xh&resize=1200:*',
    '',
    'https://res.akamaized.net/domain/image/upload/t_web/v1538713881/bigsmall_Mirvac_house2_twgogv.jpg',
  ];
    
  onMount(() => {
    // Fetch product images or perform any other initialization logic
  });

</script>
  
  <!-- <style>
    .grid-container {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 1rem;
    }
    
    .product-image {
      width: 100%;
      height: auto;
    }
  </style> -->

  <div class="flex flex-row flex-wrap">
  
      <div class="w-full xl:w-4/6 relative xl:pr-2">
        <img class="w-full rounded-3xl object-cover aspect-[4/3] md:aspect-[16/9]" src="https://img.staticmb.com/mbcontent/images/uploads/2022/12/Most-Beautiful-House-in-the-World.jpg" alt="Product"/>
      </div>
      <div class="hidden xl:grid grid-cols-3 grid-rows-3 xl:w-2/6 gap-2 rounded-3xl overflow-hidden">
        <div class="col-span-2 row-span-1 bg-slate-400 rounded-[10px]"></div>
        <div class=" col-span-1 bg-white rounded-[10px]"></div>
        <div class=" row-span-2 bg-pink-500 rounded-[10px]"></div>
        <div class=" col-span-1 bg-cyan-500 rounded-[10px]"></div>
        <div class=" col-span-1 bg-fuchsia-500 rounded-[10px]"></div>
        <div class=" col-span-1 bg-purple-500 rounded-[10px]"></div>
        <div class=" col-span-1 bg-gray-50/20 rounded-[10px] hover:bg-white/30  transition-colors ease-linear duration-300 overflow-hidden"></div>
      </div>
      <!-- <div class="col-span-full ">
        <Contact />
      </div> -->
  </div>


