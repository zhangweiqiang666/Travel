<template>
  <div>
    <home-header></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :list="iconList"></home-icons>
    <home-recommend :list="sightList"></home-recommend>
    <home-youlike :list="youLikeList"></home-youlike>
    <home-weekend :list="weekendList"></home-weekend>
  </div>
</template>

<script>
import axios from 'axios'
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeYoulike from './components/YouLike'
import HomeWeekend from './components/Weekend'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeYoulike,
    HomeWeekend
  },
  mounted () {
    this.getHomeInfo()
  },
  data () {
    return {
      swiperList: [],
      iconList: [],
      sightList: [],
      weekendList: [],
      youLikeList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json').then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data.data
      this.swiperList = res.swiperList
      this.iconList = res.iconList
      this.sightList = res.sightList
      this.weekendList = res.weekendList
      this.youLikeList = res.youLikeList
      console.log(res);
      
    }
  }
}
</script>

<style scoped >
</style>
