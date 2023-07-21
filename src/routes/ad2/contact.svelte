	
<script lang="ts">
	import Badge from "$components/ui/badge/Badge.svelte";
    import { Button } from "$components/ui/button";

</script>

<!-- <div class="w-full h-[1px] bg-gradient-to-r from-transparent via-fuchsia-200/80"></div> -->
<div class="w-full  rounded-3xl flex flex-row items-center shadow-inner shadow-gray-800">
    <div class="px-3 py-3">
        <img class=" h-14 w-14 rounded-full object-cover" src="https://cdn.britannica.com/45/5645-050-B9EC0205/head-treasure-flower-disk-flowers-inflorescence-ray.jpg" alt="Seller Profile">
    </div>
    <div class="flex flex-col shrink">
        <p class="text-xl text-primary-foreground font-semibold">Delux imobiliare</p>
        <Badge class="w-fit dark bg-fuchsia-200">Agentie imobiliara</Badge>
    </div>
    <div class="ml-4">
        <Button class="dark font-semibold hover:translate-y-0.5  transition duration-300">
            Contact
        </Button>
        <Button variant="secondary" class="dark font-semibold bg-fuchsia-300/50 hover:bg-fuchsia-300/30 hover:translate-y-0.5  transition duration-300  ">
            Mesaj
        </Button>
    </div>
</div>

