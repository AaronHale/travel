<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="page of pages" :key="index">
        <div
          class="icon"
          v-for="icon of page"
          :key="icon.id"
        >
          <div class="icon-img">
            <img class="icon-img-content" :src="icon.imgUrl" alt="">
          </div>
          <p class="icon-desc">{{icon.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconLists: [
        {id: '001', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/8d/747c9a29b8dba402.png', desc: '景点门票'},
        {id: '002', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png', desc: '滑雪季节'},
        {id: '003', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png', desc: '景点门票'},
        {id: '004', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/8d/747c9a29b8dba402.png', desc: '景点门票景点门票'},
        {id: '005', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/8d/747c9a29b8dba402.png', desc: '景点门票'},
        {id: '006', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/8d/747c9a29b8dba402.png', desc: '景点门票'},
        {id: '007', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/8d/747c9a29b8dba402.png', desc: '景点门票'},
        {id: '008', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/8d/747c9a29b8dba402.png', desc: '景点门票'},
        {id: '009', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/8d/747c9a29b8dba402.png', desc: '一日游'}
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconLists.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        } else {
          pages[page].push(item)
        }
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import "../../../assets/styles/varibles.styl"
  @import "../../../assets/styles/mixins.styl"
  .icons >>> .swiper-container
    height:0
    padding-bottom:50%
    overflow: hidden
  .icons
    margin-top: .1rem
    .icon
      position relative
      overflow hidden
      width: 25%
      height 0
      float:left
      padding-bottom 25%
      .icon-img
        position absolute
        top 0
        left 0
        right 0
        bottom .44rem
        box-sizing border-box
        padding .1rem
        width: 80%
        margin: 0 auto
        text-align: center
        .icon-img-content
          display block
          margin 0 auto
          height 100%
    .icon-desc
      position absolute
      left 0
      right 0
      bottom 0
      height .44rem
      line-height .44rem
      text-align center
      color $darkTextColor
      ellipsis()
</style>
