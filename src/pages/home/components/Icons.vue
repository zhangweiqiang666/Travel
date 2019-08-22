<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide
        v-for="(page, index) in pages"
        :key="index"
      >
        <div
          class="icon"
          v-for="item in page"
          :key="item.id"
        >
          <div class="icon-img">
            <img
              :src="item.imgUrl"
              alt=""
            />
          </div>
          <p>{{item.desc}}</p>
        </div>
      </swiper-slide>
      <!--Optional controls -->
      <div
        class="swiper-pagination"
        slot="pagination"
      ></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcon',
  props:['list'],
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      }
    }
  },
  computed: {
    pages() {
      const pages = []
      this.list.forEach((item, index) => {
        // 计算页数
        const page = Math.floor(index / 8)
        // 如果页数不存在 返回空数组
        if (!pages[page]) {
          pages[page] = []
        }
        // 将当前图标添加到当前页上
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style scoped lang="stylus">
@import '~style/varibles.styl';
@import '~style/minins.styl';

.icons >>> .swiper-container {
  overflow: hidden;
  height: 0;
  padding-bottom: 50%;
}

.icon {
  overflow: hidden;
  position: relative;
  height: 0;
  float: left;
  width: 25%;
  padding-bottom: 22%;

  .icon-img {
    width: 100%;
    height: 70%;
    position: absolute;
    margin: auto;

    img {
      display: block;
      margin: 0 auto;
      height: 100%;
    }
  }

  p {
    color: $darkTextColor;
    width: 100%;
    text-align: center;
    position: absolute;
    bottom: 0.1rem;
    ellipsis();
  }
}
</style>
