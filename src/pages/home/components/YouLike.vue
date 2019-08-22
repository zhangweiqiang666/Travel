<template>
  <div>
    <div class="title"><span class="iconfont">&#xe635;</span>猜你喜欢</div>
      <ul>
        <li v-for="(item, index) in youLikeList" :key="index">
          <div class="list-img">
            <div class="tag"><img :src="item.tagUrl" alt="" /><i>{{item.tagTitle}}</i></div>
            <div class="main-img"><img :src="item.imgUrl" alt=""></div>
          </div>
          <div class="list-msg">
            <div class="address">{{item.address}}</div>
            <div class="comment"><span class="iconfont" v-html="item.star"></span> {{item.comment}}条评论</div>
            <div class="price">￥<i>{{item.price}}</i><b> 起</b><span>{{item.place}}</span></div>
          </div>
        </li>
      </ul>
      <div class="footer">
        查看所有产品
      </div>
    </div>
</template>

<script>
export default {
  name: 'HomeYouLike',
  data () {
    return {
      youLikeList:[{
        tagTitle:'随买随用',
        tagUrl:'https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1606/5a/5a7ce7e716c8fc97e2.water.jpg_200x200_090bb108.jpg',
        address:'碧海银沙（启东恒大世纪旅游城）',
        place:'启东市',
        star:'&#xe62a;&#xe62a;&#xe62a;&#xe62a;&#xe62a;',
        comment:1037,
        price:55,
      },{
        tagTitle:'随买随用',
        tagUrl:'https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1606/5a/5a7ce7e716c8fc97e2.water.jpg_200x200_090bb108.jpg',
        address:'碧海银沙（启东恒大世纪旅游城）',
        place:'启东市',
        star:'&#xe62a;&#xe62a;&#xe62a;&#xe62a;&#xe62a;',
        comment:1037,
        price:55,
      },{
        tagTitle:'随买随用',
        tagUrl:'https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1606/5a/5a7ce7e716c8fc97e2.water.jpg_200x200_090bb108.jpg',
        address:'碧海银沙（启东恒大世纪旅游城）',
        place:'启东市',
        star:'&#xe62a;&#xe62a;&#xe62a;&#xe62a;&#xe62a;',
        comment:1037,
        price:55,
      },{
        tagTitle:'随买随用',
        tagUrl:'https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1606/5a/5a7ce7e716c8fc97e2.water.jpg_200x200_090bb108.jpg',
        address:'碧海银沙（启东恒大世纪旅游城）',
        place:'启东市',
        star:'&#xe62a;&#xe62a;&#xe62a;&#xe62a;&#xe62a;',
        comment:1037,
        price:55,
      },{
        tagTitle:'随买随用',
        tagUrl:'https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1606/5a/5a7ce7e716c8fc97e2.water.jpg_200x200_090bb108.jpg',
        address:'碧海银沙（启东恒大世纪旅游城）',
        place:'启东市',
        star:'&#xe62a;&#xe62a;&#xe62a;&#xe62a;&#xe62a;',
        comment:1037,
        price:55,
      },{
        tagTitle:'随买随用',
        tagUrl:'https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1606/5a/5a7ce7e716c8fc97e2.water.jpg_200x200_090bb108.jpg',
        address:'碧海银沙（启东恒大世纪旅游城）',
        place:'启东市',
        star:'&#xe62a;&#xe62a;&#xe62a;&#xe62a;&#xe62a;',
        comment:1037,
        price:55,
      }]
    }
  },
  components: {}
}
</script>

<style scoped lang="stylus">
  @import '~style/minins.styl'
  .title
    height 1rem
    line-height 1rem
    text-indent .2rem
    font-size .32rem
    span
      margin-right .1rem
      color #ff6053
  ul>li
    overflow hidden
    position relative
    padding 0 .2rem .4rem
    .list-msg
      width calc(100% - 2.4rem)
      padding 0 0 0 .2rem
    .list-img,.list-msg
      float left
      .main-img
        height 2.2rem
        width 2.2rem
        img
          width 2.2rem
      .tag
        position absolute
        width 1.1rem
        img
          position absolute
          
          width 100% 
        i
          top .1rem
          position absolute
          color #fff
          font-size .24rem
      .address
        margin-top .26rem
        font-size .36rem
        ellipsis()
      .comment
        margin-top .3rem
        span
          color #ffc466
          margin-right .2rem
      .price
        width 100%
        margin-top .3rem
        color #ffc466
        b
          color #818181
        i
          font-size .40rem
        span
          color #818181
          float right
  .footer
    text-align center
    line-height .8rem
    height .8rem
    color #00afc7
    border-top .05rem solid #eee
</style>
