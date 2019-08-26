<template>
  <div class="wrapper">
    <swiper
      :options="swiperOption"
      ref="mySwiper"
      v-if="showSwiper"
    >
      <!-- slides -->
      <swiper-slide
        v-for="item in list"
        :key="item.id"
      ><img
          class="swiper-img"
          :src="item.imgUrl"
          alt="找不到图片啦！！"
        ></swiper-slide>
      <!-- Optional controls -->
      <div
        class="swiper-pagination"
        slot="pagination"
      ></div>
    </swiper>
  </div>
</template>

<script>
export default {
  props: ['list'],
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        autoplay: 3000,
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style scoped lang="stylus">
.wrapper >>> .swiper-pagination-bullet-active {
  background-color: #fff;
}

.wrapper {
  background-color: #eee;
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 26.666%;

  .swiper-img {
    width: 100%;
  }
}
</style>
