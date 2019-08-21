<template>
  <div class="container">
    <div class="recommend-title"><span class="iconfont">&#xe63f;</span>本周热门榜单 <a href="">全部榜单 <i class="iconfont">&#xe602;</i></a>
    </div>
    <ul class="rank">
      <li v-for="(item, index) in sightList" :key="index">
        <img class="topimg" v-if="item.topImg" :src="item.topImg" alt="">
        <img :src="item.imgUrl" alt="" />
        <p>{{item.name}}</p>
        <p class="priColor"
        >￥{{item.price}}<i class="pri"> 起</i></p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      sightList:[{
        topImg:'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
        name:'故宫',
        price:60
      },{
         topImg:'http://img1.qunarzz.com/piao/fusion/1710/2d/36d0c4adaebbbc02.png',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
        name:'故宫',
        price:60
      },{
         topImg:'http://img1.qunarzz.com/piao/fusion/1710/67/edc47ffef9e96b02.png',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
        name:'故宫',
        price:60
      },{
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
        name:'故宫',
        price:60
      },{
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
        name:'故宫',
        price:60
      },{
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
        name:'故宫',
        price:60
      },{
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
        name:'故宫',
        price:60
      }]
    }
  },
  components: {}
}
</script>

<style scoped lang="stylus">
  .container
    border-top .25rem solid #eee
    border-bottom  .25rem solid #eee
  .recommend-title
    line-height .8rem
    text-indent .2rem
    span.iconfont
      color #ff7448
    a
      float right
      color #616161  
  .rank
    height 3.2rem
    white-space nowrap
    overflow-x scroll
    li
      position relative
      display inline-block
      margin-left .3rem
      margin-top .2rem
      img
        height 2rem
      .topimg
        width 1rem
        position absolute
        top -.1rem
        height .4rem
      p
        text-align center
        margin-top .1rem
      .priColor
        color #ffb436
        .pri
          color #616161

</style>
