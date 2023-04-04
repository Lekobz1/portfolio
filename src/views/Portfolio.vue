<template>
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