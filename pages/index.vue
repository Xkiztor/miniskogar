<script setup lang='ts'>

const karusellNumber = ref(0)

const karusellItemCount = ref(8)

const karusellLeft = () => {
  if (karusellNumber.value !== 0) karusellNumber.value--

}

const karusellRight = () => {
  if (karusellNumber.value !== 5 - 1) karusellNumber.value++
}

</script>


<template>
  <main class="page index">
    <header>
      <div class="text">
        <h1>Miniskogar</h1>
        <h2>"Skogsbada mitt i staden"</h2>
      </div>
      <img src="http://lindersplantskola.se/wp/wp-content/uploads/2015/03/IMG_8212_resize.jpg" alt="">
    </header>
    <section class="vad-är">
      <dl>
        <dt>
          <h1>Vad är en miniskog?</h1>
        </dt>
        <dd>
          <p>En miniskog är en liten planterad skog som på kort tid kan skapa en skogskänsla på en tidigare tom plats.
            Konceptet med miniskogar eller mikroskogar som det också kallas sprids nu fort över världen. Detta är en bra
            sätt att engagera människor och visa på trädens många värden. Med miniskogar kan vi t.ex. på en liten
            restyta i en stad snabbt få upp en härlig skog för människor att fly in och “skogsbada” i under stekheta
            sommardagar. På blåsiga vinterdagar kan man få lite vindskydd och året om kan den lilla skogen vara en källa
            till naturupplevelser, kanske bara några meter från en öppen stadsmiljö.
            Miniskogar kan vara av många olika slag men gemensamt för konceptet är att man snabbt når en frodig
            skogskänsla genom att plantera riktigt tätt med små plantor som sedan skyddar varandra, tävlar om
            höjdtillväxten och bildar små ekosystem.
            Löv och grenar får ligga kvar i miniskogen och bidra till mullhalten och bomiljön för insekter m.m.
            En miniskog kan ha många relevanta syften i dagens värld. Såsom skuggskapande, temperatursänkning,
            dagvattenfördröjning, kolinlagring, underlag för biologisk mångfald, rekreation m.m., m.m.
            Ett klokt val är att också låta miniskogen vara en matskog med mycket ätliga växter för att på ett mycket
            hållbart sätt bidra lite till framtidens matförsörjning. En miniskog är ett perfekt sätt att engagera
            medborgarna till att delta, plantera, beskära, skörda, lära av och njuta av skogen.
          </p>
        </dd>
      </dl>
    </section>
    <section class="karusell">
      <button class="karusell-button" @click="karusellLeft()" :disabled="karusellNumber === 0">←</button>
      <div class="karusell-container">
        <div class="karusell-items left"
          :style="{ transform: `translateX(${(karusellNumber * -70) - (karusellNumber * 20)}ch)` }">
          <div>
            <img src="https://oykwqfkocubjvrixrunf.supabase.co/storage/v1/object/public/bilder/IMG_8116.JPG" alt="">
            <div>
              <h1>Matskog/Skogsträdgård</h1>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam hic necessitatibus omnis modi,
                perferendis atque ratione alias assumenda sapiente maxime eius odio nam debitis, fuga a doloremque
                perspiciatis ut in explicabo, id provident veritatis recusandae? Dolor laborum fugit quae adipisci.</p>
            </div>

          </div>
          <div>
            <img src="" alt="">
            <div>
              <h1>Ätliga beträdor </h1>
            </div>

          </div>
          <div>
            <img src="" alt="">
            <div>
              <h1>Nötlund</h1>
            </div>

          </div>
          <div>
            <img src="" alt="">
            <div>
              <h1>Klätterskog</h1>
            </div>

          </div>
          <div>
            <img src="" alt="">
            <div>
              <h1>Dagisskog/Skolskog</h1>
            </div>

          </div>
          <div>
            <img src="" alt="">
            <div>
              <h1>Miniurskog</h1>
            </div>

          </div>
          <div>
            <img src="" alt="">
            <div>
              <h1>Magnoliaskog</h1>
            </div>

          </div>
          <div>
            <img src="" alt="">
            <div>
              <h1>Designskog</h1>
            </div>

          </div>
        </div>
      </div>
      <button class="karusell-button right" @click="karusellRight()"
        :disabled="karusellNumber === karusellItemCount - 1">→</button>
    </section>
  </main>
</template>


<style>
.index header {
  width: 100%;
  display: grid;
  place-items: center;
  height: 30rem;
  overflow: hidden;
  /* z-index: 2; */
  position: relative;
}

.index header .text {
  padding: 1rem 10rem;
  /* position: absolute; */
  text-align: center;
  color: white;
  z-index: 2;
  text-shadow: 0 0 15px rgba(0, 0, 0, 0.8);
}

.index header .text h1 {
  font-size: 8rem;
  margin-bottom: 1rem;
  margin: 0;
  font-weight: 900;
}

.index header .text h2 {
  font-size: 3rem;
  margin-bottom: 1rem;
  margin: 0;
  font-weight: 700;
}


.index header img {
  width: 100%;
  position: absolute;
  z-index: 1;
  filter: brightness(80%);
}

.index section {
  display: grid;
  place-items: center;
  width: 100%;
  padding: 4rem;
}

.index section dl {
  width: 70ch;
}

section.karusell {
  /* position: relative; */
  gap: 1rem;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;

}

section.karusell * {
  transition: all 0.5s ease-in-out;
}

.karusell-container {
  width: 70ch;
  height: 40rem;
  overflow: hidden;
  position: relative;
  border-radius: 1rem;
}

.karusell-items {
  display: flex;
  flex-direction: row;
  position: absolute;
  height: 100%;
  gap: 20ch;
}

.karusell-items>div {
  height: 100%;
  width: 70ch;
  background: var(--element-bg);
  border-radius: 1rem;
  display: grid;
  grid-template-rows: 60% 40%;
  grid-template-columns: 1fr;
}

.karusell-items>div>img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 1rem;
  box-shadow: 0 0 15px #434714;
}

.karusell-items>div>div {
  padding: 1rem;
}



.karusell-button {
  /* position: absolute;
  top: 50%;
  transform: translateY(-50%); */
}

.karusell-button:disabled {
  opacity: 0.5;
}
</style>