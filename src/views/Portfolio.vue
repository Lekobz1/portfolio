<template>
   <div class="banniere-img">
    <div class="banniere">
      <h2>{{ message }} et bienvenu sur mon portfolio</h2>
    </div>
  </div>
  <swiper
    :effect="'coverflow'"
    :grabCursor="true"
    :centeredSlides="true"
    :slidesPerView="'auto'"
    :coverflowEffect="{
      rotate: 50,
      stretch: 0,
      depth: 100,
      modifier: 1,
      slideShadows: true,
    }"
    :pagination="true"
    :modules="modules"
    class="mySwiper"
  >
    <swiper-slide><img src="../assets/photocar.jpg" /> <p>Gallerie photo</p></swiper-slide>
    <swiper-slide><img src="../assets/videocar.jpg" /> <p>Gallerie Video</p></swiper-slide>
    <swiper-slide><img src="../assets/devcar.jpg" /> <p> Projet digitaux</p></swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/effect-coverflow";
import "swiper/css/pagination";

// import required modules
import { EffectCoverflow, Pagination } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [EffectCoverflow, Pagination],
    };
  },
};
</script>

<style scoped>

h2{
  grid-area: title; 
    font-family: 'Montserrat', sans-serif;
    font-weight: 700;
    text-transform: uppercase;
    color: white;
    font-size: 55px;
}
.banniere-img{
    height: 50vh;
    background-image: url(../assets/test.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-position: top center;
    position: relative;
    z-index: 1;
}

.banniere-img::after{
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    height: 100%;
    width: 100%;
    background-color: black;
    opacity: 0.45;
    z-index: -1;
}
.banniere {  
    display: grid;
    height: 100%;
    grid-template-columns: 100%;
    grid-template-rows: 25% 25% 25% 25%;
    grid-auto-columns: 1fr;
    gap: 0% 0%;
    grid-auto-flow: row;
    grid-template-areas:
        "."
        "title"
        "buttons"
        ".";
    text-align: center;
}
.swiper {
  width: 100%;
  padding-top: 150px;
  padding-bottom: 100px;
}

.swiper-slide {
  background-position: center;
  background-size: cover;
  width: 600px;
  height: 600px;
}

.swiper-slide img {
  display: block;
  width: 100%;
}

p{
  font-size: xx-large;
  text-align: center;
  text-transform: uppercase;
  color: rgba(37, 35, 35, 1);
}
</style>