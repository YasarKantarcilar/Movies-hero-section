<script lang="ts">
  export let movieName: string;
</script>

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
    Scelerisque sed ultricies tristique. Mi in vivamus aliquam varius eu felis.
    Id ultricies diam turpis mi tincidunt. Ut morbi sed urna tempor imperdiet eu
    scelerisque egestas. Interdum mi orci suspendisse in s...
  </p>
  <div class="w-full flex gap-8 justify-start items-center">
    <button class="w-1/3 h-16 border-2 rounded-lg">Watch Trailer</button>
    <button class="w-1/3 h-16 font-bold rounded-lg text-[#373737] bg-[#F5C518]"
      >Watch Now</button
    >
  </div>
</div>
