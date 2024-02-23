<script lang="ts">
  export let isActive: boolean;
  export let movie: any = {};
  export let onClick: () => void;
</script>

<div
  aria-label={movie.title}
  aria-roledescription="movie"
  aria-pressed={isActive}
  on:click={onClick}
  class="h-[50%] md:h-[70%] aspect-[8/12] bg-white rounded-lg"
>
  <img
    alt="movie"
    src={movie.image}
    class={`w-full h-full ${
      isActive ? "grayscale-0 scale-125" : "grayscale-[80%]"
    } object-cover  rounded-lg transition-all`}
  />
</div>
