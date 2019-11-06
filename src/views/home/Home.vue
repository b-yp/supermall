<template>
  <div id="home">
    <nav-bar><div slot="center">购物街</div></nav-bar>
    <!-- 这里的轮播图使用 vue-awesome-swiper 插件 -->
    <home-swiper :banners="banners"></home-swiper>
    <p>home</p>
  </div>
</template>

<script>
import NavBar from '@/components/common/navbar/NavBar'
// import { swiper, swiperSlide } from 'vue-awesome-swiper'
import HomeSwiper from './childComps/HomeSwiper'


import { getHomeMultidata } from '@/network/home'

export default {
  name: 'Home',
  components: {
    NavBar,
    HomeSwiper
  },
  data () {
    return {
      banners: []
    }
  },
  created () {
    getHomeMultidata().then(res => {
      // console.log(res)
      this.banners = res.data.data.banner.list
      console.log(this.banners)
    })
  }
}
</script>

<style scoped>

</style>