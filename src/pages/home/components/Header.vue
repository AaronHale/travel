<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont backicon">&#xe600;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe670;</span>
      输入城市/景点/游玩/主题
    </div>
    <router-link to="city">
      <div class="header-right">
        {{this.city}}
       <!-- {{this.doubleCity}}-->
        <span class="iconfont arrowicon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
    /* ...mapGetters(['doubleCity']) */
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .header
    display: flex
    height: $headerHeight
    line-height:  $headerHeight
    background: $bgColor
    color:#fff
    .header-left
      width: 0.64rem
      .backicon{
        text-align: center
        font-size:.4rem
      }
    .header-input
      color:#ccc
      line-height:.64rem
      padding-left:.2rem
      height:.64rem
      margin-left: .2rem
      margin-top: .12rem
      flex: 1
      background: #ffffff
      border-radius: .1rem;
    .header-right
      color:#fff
      min-width:1.04rem
      text-align: center
      padding: .1rem
      .arrowicon
        font-size: .24rem
        margin-left:-0.04rem
</style>
