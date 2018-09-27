<template>
  <router-link to="/">
    <div class="header">
      城市选择
      <div class="iconfont header-back">&#xe600;</div>
    </div>
  </router-link>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import "../../../assets/styles/varibles.styl"
  .header
    position relative
    font-size: .32rem
    overflow:hidden
    height: $headerHeight
    line-height: $headerHeight
    text-align: center
    color:#fff
    background:$bgColor
    .header-back
      top:0
      left:0
      position:absolute
      width:.64rem
      text-align:center
      font-size:.4rem
      color:#fff
</style>
