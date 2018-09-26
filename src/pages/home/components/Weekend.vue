<template>
  <div >
    <div class="title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>

</template>

<script>
  export default {
    name: 'HomeWeekend',
    data() {
      return {
        recommendList: [
          {id: '0001', imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/11/1135f85716636eb090.water.jpg_640x276_75868cb8.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
          {id: '0002', imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/11/1135f85716636eb090.water.jpg_640x276_75868cb8.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
          {id: '0003', imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/11/1135f85716636eb090.water.jpg_640x276_75868cb8.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
          {id: '0004', imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/11/1135f85716636eb090.water.jpg_640x276_75868cb8.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
          {id: '0005', imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/11/1135f85716636eb090.water.jpg_640x276_75868cb8.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
          {id: '0006', imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/11/1135f85716636eb090.water.jpg_640x276_75868cb8.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
          {id: '0007', imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/11/1135f85716636eb090.water.jpg_640x276_75868cb8.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
          {id: '0008', imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/11/1135f85716636eb090.water.jpg_640x276_75868cb8.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
          {id: '0009', imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/11/1135f85716636eb090.water.jpg_640x276_75868cb8.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'}
        ]
      }
    }
  }
</script>

<style lang="stylus" scoped>
  @import "../../../assets/styles/mixins.styl"
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .3rem
  .item-img-wrapper
      overflow: hidden
      height:0
      padding-bottom:33.9%
      .item-img
        width:100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #cccccc
      ellipsis()
</style>
