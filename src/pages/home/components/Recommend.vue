<template>
  <div class="container">
    <div class="recommend-title"><span class="iconfont">&#xe63f;</span>本周热门榜单 <a href="">全部榜单 <i class="iconfont">&#xe602;</i></a>
    </div>
    <ul class="rank">
      <li
        v-for="item in list"
        :key="item.id"
      >
        <img
          class="topimg"
          v-if="item.topImg"
          :src="item.topImg"
          alt=""
        >
        <img
          :src="item.imgUrl"
          alt=""
        />
        <p>{{item.name}}</p>
        <p class="priColor">￥{{item.price}}<i class="pri"> 起</i></p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: ['list']
}
</script>

<style scoped lang="stylus">
.container {
  border-top: 0.25rem solid #eee;
  border-bottom: 0.25rem solid #eee;
}

.recommend-title {
  line-height: 0.8rem;
  text-indent: 0.2rem;

  span.iconfont {
    color: #ff7448;
  }

  a {
    float: right;
    color: #616161;
  }
}

.rank {
  height: 3.2rem;
  white-space: nowrap;
  overflow-x: scroll;

  li {
    position: relative;
    display: inline-block;
    margin-left: 0.3rem;
    margin-top: 0.2rem;

    img {
      height: 2rem;
    }

    .topimg {
      width: 1rem;
      position: absolute;
      top: -0.1rem;
      height: 0.4rem;
    }

    p {
      text-align: center;
      margin-top: 0.1rem;
    }

    .priColor {
      color: #ffb436;

      .pri {
        color: #616161;
      }
    }
  }
}
</style>
