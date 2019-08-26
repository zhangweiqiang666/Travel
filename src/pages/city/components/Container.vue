<template>
  <div class="container">
    <div class="header">
      <ul>
        <li
          @click="select('one')"
          :class={active:one}
        >境内</li>
        <li
          @click="select('two')"
          :class={active:two}
        >境外·港澳台</li>
      </ul>
    </div>
    <div class="content">
      <div v-if="one">
        <div class="title">
          热门城市
        </div>
        <ul>
          <li
            v-for="(item, index) in city.hotCities"
            :key="index"
          >
            {{item.name}}
          </li>
        </ul>
        <!-- 字母排序 -->
        <div class="title">
          字母排序
        </div>
        <ul class="letter-body">
          <li
            @click="handleClick"
            class="letter"
            v-for="(value,key, index) in city.cities"
            :key="index"
          >
            {{key}}
          </li>
        </ul>
        <!-- 城市列表 -->
        <div
          v-for="(value,key) in city.cities"
          :key="key"
        >
          <div class="title" :id="key">
            {{key}}
          </div>
          <ul>
            <li
              class="cities"
              v-for="item in value"
              :key="item.id"
            >
              {{item.name}}</li>
          </ul>
        </div>
      </div>
      <div v-if="two">

      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['city'],
  name: 'CityContainer',
  data() {
    return {
      letter:'',
      one: true,
      two: false,
    }
  },
  methods: {
    select(index) {
      this.one = 'one' === index
      this.two = 'two' === index
    },
    handleClick(e){
      this.letter= e.target.innerText
      document.querySelector("#"+this.letter).scrollIntoView(true);
    }
  }
}
</script>

<style scoped lang="stylus">
@import '~style/varibles.styl';

.container {
  .header {
    background-color: $bgColor;
    height: 0.6rem;
    text-align: center;
    color: #fff;
    padding: 0 1rem;

    ul {
      display: flex;

      li {
        height: 0.4rem;
        line-height: 0.4rem;
        flex: 1;
        border: 0.03rem solid #fff;
      }

      .active {
        background-color: #fff;
        color: $bgColor;
      }
    }
  }

  .content {
    .title {
      height: 0.72rem;
      background-color: #eee;
      line-height: 0.72rem;
      text-indent: 0.2rem;
      font-size: 0.24rem;
    }

    .letter-body {
      padding: 0.3rem 0;
    }

    ul {
      overflow: hidden;

      li {
        float: left;
        height: 0.9rem;
        line-height: 0.9rem;
        text-align: center;
        border-bottom: 0.02rem solid #ddd;
        margin-bottom: -0.02rem;
        border-right: 0.02rem solid #ddd;
        margin-right: -0.02rem;
        width: 33.33%;
      }

      .letter {
        border: none;
        width: 16.66%;
      }

      .cities {
        width: 25%;
      }
    }
  }
}
</style>
