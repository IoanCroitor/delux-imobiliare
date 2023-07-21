<script>
// @ts-nocheck

import { onMount } from 'svelte';
import { Client, Databases } from "appwrite";
import { each } from 'svelte/internal';
import Card from '$components/card.svelte';

let ad_data=[];

const client = new Client();
const databases = new Databases(client);

client
  .setEndpoint('http://localhost/v1')
  .setProject('63a44639058250c3e0f2');

onMount(async () => {
  try {
    const response = await databases.listDocuments('6401fd843046f30586b8', '6401fd8fce145e7f510a');
    ad_data = response.documents;
    console.log(ad_data); //check if the data is loaded (will return an array)
  } catch (error) {
    console.error(error);
  }
  
});

    let isRentable=true;
    let isAdFavourite=false;
    let ads=["house","4rooms","etc","house","4rooms","etc","house","4rooms","etc"];

</script>


<div class="flex flex-col items-center max-w-7xl mx-auto">
  <div class="mt-4 grid sm:grid-cols-1 md:grid-cols-2 xl:grid-cols-3 2xl:grid-cols-4 7xl:grid-cols-4 gap-5 items-center justify-evenly mx-4">
    {#each ads as ad}
      <Card />
    {/each}
  </div>  
</div>
