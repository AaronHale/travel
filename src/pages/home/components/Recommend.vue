<template>
  <div >
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>

</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [
        {id: '0001', imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
        {id: '0002', imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
        {id: '0003', imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
        {id: '0004', imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
        {id: '0005', imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
        {id: '0006', imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
        {id: '0007', imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
        {id: '0008', imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'},
        {id: '0009', imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg', title: '北京欢乐谷', desc: '远离城市喧嚣，感受自然之美'}
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
  .item
    display: flex
    height:1.9rem
    overflow:hidden
    .item-img
      width:1.7rem;
      height:1.7rem
      padding:.1rem
    .item-info
        min-width: 0
        flex:1
        padding: .1rem
        .item-title
          line-height: .54rem
          font-size: .32rem
          ellipsis()
        .item-desc
          line-height: .4rem
          color: #cccccc
        .item-button
          background:#ff9300
          margin-top: .16rem
          padding:.1rem
          color: #ffffff
          line-height:.44rem
          border-radius:.06rem
          ellipsis()
</style>
