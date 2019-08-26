<template>
  <div class="header">
    <div class="header-left"><span class="iconfont">&#xe624;</span></div>
    <div class="header-input"><span class="iconfont">&#xe632;</span><input
        type="text"
        placeholder="输入城市/景点/游玩主题"
      > </div>
    <router-link to="/city">
      <div class="header-right">城市<span class="iconfont">&#xe600;</span></div>
    </router-link>
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
@import '~style/varibles.styl';

.header {
  line-height: 0.86rem;
  display: flex;
  height: 0.86rem;
  background-color: $bgColor;
  color: #fff;

  .header-left {
    text-align: center;
    width: 0.9rem;
    float: left;
  }

  .header-input {
    line-height: 0.64rem;
    color: #ccc;
    flex: 1;
    background: #fff;
    margin-top: 0.12rem;
    height: 0.64rem;
    border-radius: 0.1rem;

    input {
      position: relative;
      top: -0.05rem;
      display: inline-block;
      height: 0.6rem;
      width: 4.4rem;
      margin: 0 0.2rem;
    }

    span {
      display: inline-block;
      font-size: 0.4rem;
      margin-left: 0.1rem;
    }
  }

  .header-right {
    color: #fff;
    width: 1.24rem;
    float: right;
    text-align: center;
  }
}
</style>
