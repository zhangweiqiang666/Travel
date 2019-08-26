<template>
  <div class="header">

    <router-link to="/">
      <div>
        <span class="iconfont">&#xe624;</span>
      </div>
    </router-link>

    城市选择
  </div>
</template>

<script>
export default {
  name: 'CityHeader',
  data() {
    return {}
  },
  components: {}
}
</script>

<style scoped lang="stylus">
@import '~style/varibles.styl';

.header {
  background-color: $bgColor;
  height: 0.86rem;
  line-height: 0.86rem;
  position: relative;
  color: #fff;
  font-size: 0.34rem;
  text-align: center;

  div {
    position: absolute;
    top: 0;
    left: 0;
    font-weight: 700;
    width: 0.86rem;
    color: #fff;
  }
}
</style>
