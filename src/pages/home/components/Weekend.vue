<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul class="weekend-list">
      <li
        v-for="item in list"
        :key="item.id"
      >
        <div><img
            :src="item.imgUrl"
            alt=""
          ></div>
        <p>{{item.title}}</p>
        <p class="desc">{{item.desc}}</p>
      </li>
    </ul>
    <div class="footer">① <i>票面价</i>是指通过景区指定窗口售卖的纸质门票上标注的价格</div>
  </div>
</template>

<script>
export default {
  props: ['list'],
  name: 'HomeWeekend',
  data () {
    return {}
  },
  components: {}
}
</script>

<style scoped lang="stylus">
@import '~style/minins.styl';

.title {
  background-color: #f5f5f5;
  height: 0.8rem;
  line-height: 0.8rem;
  font-size: 0.34rem;
  text-indent: 0.2rem;
}

.weekend-list {
  li {
    border-bottom: 0.16rem solid #eee;

    img {
      width: 100%;
    }

    p {
      margin: 0.25rem 0;
      text-indent: 0.2rem;
      ellipsis();
      padding-right: 1rem;
    }

    .desc {
      font-size: 0.24rem;
      color: #616161;
    }
  }
}

.footer {
  color: #616161;
  height: 0.7rem;
  line-height: 0.7rem;
  text-indent: 0.2rem;
  font-size: 0.24rem;

  i {
    font-weight: 700;
  }
}
</style>
