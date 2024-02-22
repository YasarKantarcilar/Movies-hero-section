<script lang="ts">
  export let data: any[] = [];
</script>

{#each data as item}
  <div class="aspect-square bg-black flex flex-col">
    <img src={item.thumbnail} class="w-full h-[90%]" alt="product" />
    <div class="w-full h-[10%] flex justify-around items-center">
      <p class="text-white">{item.brand}</p>
      <p class="text-white">{item.price}</p>
    </div>
  </div>
{/each}
