<script lang="ts">
import Star from "$icons/star.svelte";
type StarType = 'filled' | 'halfFilled' | 'unfilled';

export let rating: number = 3.7;

type Star = {
    type: StarType;
    class: string;
};

export let starArr: Star[] = [];

for (let i = 0; i < Math.floor(rating); i++) {
    starArr.push({ type: 'filled', class: `fill-fuchsia-300` });
}

if (rating % 1 >= 0.25 && rating % 1 < 0.75) {
    starArr.push({ type: 'halfFilled', class: `fill-fuchsia-300` });
} else if (rating % 1 >= 0.75) {
    starArr.push({ type: 'filled', class: `fill-fuchsia-300` });
}

while (starArr.length < 5) {
    starArr.push({ type: 'unfilled', class: `fill-fuchsia-300/60` });
}
console.log(starArr);
</script>

<div class="hidden md:flex flex-row place-items-center">
    <p class="text-white text-2xl font-semibold pr-1">{rating}</p>
    {#each starArr as star}
        <Star variant={star.type} class={`w-6 h-6 ${star.class}`} />
    {/each}
</div>
<div class="md:hidden flex flex-row place-items-center">
    <p class="text-white text-2xl font-semibold pr-1">{rating}</p>
    <Star variant={starArr[0].type} class={`w-6 h-6 ${starArr[0].class}`} />
</div>


