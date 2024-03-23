<script setup lang='ts'>

</script>


<template>
  <div class="page about">
    <img class="big-img" src="https://lundstradgardssallskap.se/wp-content/uploads/Peter-Linder.gif" alt="">
    <div>
      <h1>Om oss</h1>
      <p>Jag som driver denna hemsida heter Peter Linder, är trädgårdsingenjör och plantskolist och brinner för växter
        av
        alla slag. Särskilt ätliga miniskogar ligger mig varmt om hjärtat. Att få bidra till en lite bättre värld i både
        det lilla och det stora genom att visa på växters möjligheter ser jag som jätteroligt och jätteviktigt.
        Jag driver också Linders Plantskola (länka!) som är en liten plantskola för ovanliga växter utanför Hörby mitt i
        Skåne. På gården planterar vi också flera miniskogar eller Linderslunds Arboretum som vi kallar det.</p>
    </div>
  </div>
</template>


<style>
.page.about {
  padding: 0 2rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  max-width: 150ch;
  margin: 5rem auto 5rem;
  gap: 1rem;
  text-align: justify;
}

.page.about img {
  border-radius: 1rem;
}

@media screen and (max-width: 700px) {
  .page.about {
    grid-template-columns: 1fr;
  }
}
</style>