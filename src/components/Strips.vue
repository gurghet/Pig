<template>
  <div class="strips">
    <article>
      <h1>{{title}}</h1>
      <swiper :options="swiperOption" class="trytry">
        <swiper-slide v-for="(slide, index) in vignette" :key="index">I'm Slide {{ slide }}</swiper-slide>
        <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div>
      </swiper>
      <!--img :src="vignetta" :alt="alt"-->
    </article>
  </div>
</template>

<script>
import "swiper/dist/css/swiper.css";
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  name: "Strips",
  data() {
    return {
      title: "Cake PoC",
      vignetta: "https://via.placeholder.com/474x474",
      vignette: ["1", "2", "3", "4", "5", "6", "7"],
      alt: "example alt",
      swiperOption: {
        direction: "vertical",
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        }
      }
    };
  },
  components: {
    swiper,
    swiperSlide
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.trytry {
  height: 474px;
  width: auto;
}
</style>
