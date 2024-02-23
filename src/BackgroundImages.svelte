<script lang="ts">
  export let image: string;
</script>

<div class="absolute w-full h-screen -z-50 top-0 left-0 flex">
  <img
    src={image}
    alt="banner"
    class="w-1/3 h-screen md:flex hidden -z-50 -scale-x-100 object-cover"
  />
  <img
    src={image}
    alt="moviebanner"
    class="w-full md:w-2/3 h-auto -z-50 object-cover"
  />
</div>
