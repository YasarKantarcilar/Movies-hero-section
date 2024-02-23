<script lang="ts">
  import spidermanImage from "./assets/spiderman.png";
  import aquamanImage from "./assets/aquaman.jpg";
  import homecomingImage from "./assets/homecoming.jpg";
  import xmenImage from "./assets/xmen.jpg";
  import xmen3Image from "./assets/xmen3.jpg";
  import xmenlaststandImage from "./assets/xmenlaststand.jpg";
  import infinitywarImage from "./assets/infinitywar.png";
  import avangersImage from "./assets/avangers.jpg";
  import endgameImage from "./assets/endgame.png";
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
  <div
    class="w-full md:w-1/2 h-1/2 flex pl-[5%] md:pl-[10%] gap-5 flex-col items-start text-white justify-start"
  >
    <p class="text-5xl font-bold">{movieName}</p>
    <div class="flex w-full h-8 gap-4 justify-start items-start">
      <div
        class="w-auto font-bold h-auto px-2 rounded bg-[#F5C518] text-black text-lg"
      >
        IMDB
      </div>
      <div class="font-light text-slate-50">8.2 (12.872)</div>
      <div class="font-light text-slate-50">2021</div>
      <div class="font-light text-slate-50">| 1 hour 55 minutes |</div>
      <div class="font-light text-slate-50">Sci-fi</div>
    </div>
    <p>
      Scelerisque sed ultricies tristique. Mi in vivamus aliquam varius eu
      felis. Id ultricies diam turpis mi tincidunt. Ut morbi sed urna tempor
      imperdiet eu scelerisque egestas. Interdum mi orci suspendisse in s...
    </p>
    <div class="w-full flex gap-8 justify-start items-center">
      <button class="w-1/3 h-16 border-2 rounded-lg">Watch Trailer</button>
      <button
        class="w-1/3 h-16 font-bold rounded-lg text-[#373737] bg-[#F5C518]"
        >Watch Now</button
      >
    </div>
  </div>
  <div
    class="w-screen flex-nowrap overflow-x-scroll px-[8%] md:px-[10%] h-1/2 flex justify-start items-center z-50 gap-10 md:gap-8"
  >
    {#each movies as movie, index (index)}
      <div
        on:click={() => {
          selectedIndex = index;
          bgImage = movie.image;
          movieName = movie.title;
        }}
        class="h-[50%] md:h-[70%] aspect-[8/12] bg-white rounded-lg"
      >
        <img
          alt="movie"
          src={movie.image}
          class={`w-full h-full ${
            selectedIndex === index
              ? "grayscale-0 scale-125"
              : "grayscale-[80%]"
          } object-cover  rounded-lg transition-all`}
        />
      </div>
    {/each}
  </div>
  <div class="absolute w-full h-screen -z-50 top-0 left-0 flex">
    <img
      src={bgImage}
      alt="banner"
      class="w-1/3 h-screen sr-only md:not-sr-only -z-50 -scale-x-100 object-cover"
    />
    <img
      src={bgImage}
      alt="moviebanner"
      class="w-full md:w-2/3 h-auto -z-50 object-cover"
    />
  </div>
</div>
