<template>
  <swiper class="home-swiper" :options="swiperOption">
    <swiper-slide v-for="(item, index) in banners" :key="index">
      <a :href="item.link">
        <img :src="item.image" alt="">
      </a>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>  
</template>

<script>
import {swiper, swiperSlide} from 'vue-awesome-swiper'

export default {
  name: 'HomeSwiper',
  components: {
    swiper,
    swiperSlide
  },
  props: {
    banners: Array
  },
  data() {
    return {
      swiperOption: {
        loop: true,
        autoplay: true,
        pagination: {
          el: '.swiper-pagination'
        }
      }
    }
  }
}
</script>

<style scoped>
  @import '~swiper/dist/css/swiper.css';

  .home-swiper img {
    width: 100%;
  }
</style>