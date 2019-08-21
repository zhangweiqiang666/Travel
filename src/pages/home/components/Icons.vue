<template>
  <div class="icons" >
    <swiper :options="swiperOption">
      
      <swiper-slide v-for="(page, index) in pages" :key="index">
    <div class="icon" v-for="item in page" :key="item.id">
      <div class="icon-img">
      <img :src="item.imgUrl" alt=""/>
      </div>
      <p>{{item.desc}}</p>  
    </div>
    </swiper-slide>
          <!--Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  data () {
    return {
      swiperOption: {
      pagination: '.swiper-pagination',
      },
      iconList: [{
        id: 1001,
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '热门景点'
      },
      {
        id: 1002,
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
        desc: '故宫'
      },
      {
        id: 1003,
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        desc: '北京必游'
      },
      {
        id: 1004,
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        desc: '水上乐园'
      },
      {
        id: 1005,
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        desc: '一日游'
      },
      {
        id: 1006,
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/67/9a1678221b8e0e02.png',
        desc: '古北水镇'
      },
      {
        id: 1007,
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
        desc: '动植物园'
      },
      {
        id: 1008,
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
        desc: '奥林匹克塔'
      },
      {
        id: 1009,
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/b4511345827006994aa1980a3886f0ac.png',
        desc: '北京世园会'
      },
      {
        id: 1010,
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/bf88c62458044ca2ef9d733690eef3fc.png',
        desc: '优惠券'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
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
  @import '~style/varibles.styl'
  @import '~style/minins.styl'
  .icons >>> .swiper-container
    overflow hidden
    height 0
    padding-bottom 50%
  .icon
    overflow hidden
    position relative
    height 0
    float left
    width 25%
    padding-bottom 22%
    .icon-img
      width 100%
      height 70%
      position absolute
      margin auto
      img
        display block
        margin 0 auto
        height 100%
    p
      color $darkTextColor
      width 100%
      text-align center
      position absolute
      bottom .1rem
      ellipsis()
</style>
