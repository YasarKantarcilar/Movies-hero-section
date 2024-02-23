<script lang="ts">
  import spidermanImage from "./assets/spiderman.png";
  import aquamanImage from "./assets/aquaman.jpg";
  import homecomingImage from "./assets/homecoming.jpg";
  import xmenImage from "./assets/xmen.jpg";
  import xmen3Image from "./assets/xmen3.jpg";
  import xmenlaststandImage from "./assets/xmenlaststand.jpg";
  import avangersImage from "./assets/avangers.jpg";
  import MovieCard from "./MovieCard.svelte";
  import BackgroundImages from "./BackgroundImages.svelte";
  import MovieInfo from "./MovieInfo.svelte";
  let movies = [
    {
      image: spidermanImage,
      title: "Spiderman: No Way Home",
    },
    {
      image: aquamanImage,
      title: "Aquaman",
    },
    {
      image: homecomingImage,
      title: "Spiderman: Homecoming",
    },
    {
      image: xmenImage,
      title: "X-Men: Days of Future Past",
    },
    {
      image: xmen3Image,
      title: "X-Men",
    },
    {
      image: xmenlaststandImage,
      title: "X-Men: The Last Stand",
    },
    {
      image: avangersImage,
      title: "Avangers: Infinity War",
    },
    {
      image: spidermanImage,
      title: "Spiderman: No Way Home",
    },
    {
      image: spidermanImage,
      title: "Spiderman: No Way Home",
    },
    {
      image: aquamanImage,
      title: "Aquaman",
    },
    {
      image: homecomingImage,
      title: "Spiderman: Homecoming",
    },
    {
      image: xmenImage,
      title: "X-Men: Days of Future Past",
    },
    {
      image: xmen3Image,
      title: "X-Men",
    },
    {
      image: xmenlaststandImage,
      title: "X-Men: The Last Stand",
    },
    {
      image: avangersImage,
      title: "Avangers: Infinity War",
    },
    {
      image: spidermanImage,
      title: "Spiderman: No Way Home",
    },

    {
      image: spidermanImage,
      title: "Spiderman: No Way Home",
    },
    {
      image: aquamanImage,
      title: "Aquaman",
    },
    {
      image: homecomingImage,
      title: "Spiderman: Homecoming",
    },
    {
      image: xmenImage,
      title: "X-Men: Days of Future Past",
    },
    {
      image: xmen3Image,
      title: "X-Men",
    },
    {
      image: xmenlaststandImage,
      title: "X-Men: The Last Stand",
    },
    {
      image: avangersImage,
      title: "Avangers: Infinity War",
    },
    {
      image: spidermanImage,
      title: "Spiderman: No Way Home",
    },
  ];
  let bgImage = spidermanImage;
  let selectedIndex = 0;
  let movieName = "Spider man: No Way Home";
</script>

<div
  class="w-full from-black via-transparent to-black bg-gradient-to-b md:bg-gradient-to-r md:from-black from-15% md:to-transparent h-screen relative pt-[5%]"
>
  <MovieInfo {movieName} />
  <div
    class="w-screen flex-nowrap overflow-x-scroll px-[8%] md:px-[10%] h-1/2 flex justify-start items-center z-50 gap-10 md:gap-8"
  >
    {#each movies as movie, index (index)}
      <MovieCard
        isActive={selectedIndex === index}
        {movie}
        onClick={() => {
          selectedIndex = index;
          bgImage = movie.image;
          movieName = movie.title;
        }}
      />
    {/each}
  </div>
  <BackgroundImages image={bgImage} />
</div>
