<template>
  <div class="header">
    <div class="header-left"><span class="iconfont">&#xe624;</span></div>
    <div class="header-input"><span class="iconfont">&#xe632;</span><input type="text" placeholder="输入城市/景点/游玩主题"> </div>
    <div class="header-right">城市<span class="iconfont">&#xe600;</span></div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  data () {
    return {}
  },
  components: {}
}
</script>

<style scoped lang="stylus">
  @import '~style/varibles.styl'
  .header
    line-height .86rem
    display flex
    height .86rem
    background-color $bgColor
    color #fff
    .header-left
      text-align center
      width .9rem
      float left
    .header-input
      line-height .64rem
      color #ccc
      flex 1
      background #fff
      margin-top .12rem
      height .64rem
      border-radius .1rem
      input
        position relative
        top -.05rem
        display inline-block
        height .6rem
        width 4.4rem
        margin 0 .2rem
      span
        display inline-block
        font-size .4rem
        margin-left .1rem
    .header-right
      width 1.24rem
      float right
      text-align center
</style>
