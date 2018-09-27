<template>
    <ul class="list">
      <li class="item">A</li>
      <li class="item">B</li>
      <li class="item">C</li>
      <li class="item">D</li>
      <li class="item">E</li>
      <li class="item">F</li>
      <li class="item">G</li>
      <li class="item">H</li>
      <li class="item">I</li>
      <li class="item">J</li>
      <li class="item">K</li>
      <li class="item">L</li>
      <li class="item">M</li>
      <li class="item">N</li>
      <li class="item">O</li>
      <li class="item">P</li>
      <li class="item">Q</li>
    </ul>
</template>

<script>
export default {
  name: 'CityAlphabel'
}
</script>

<style lang="stylus" scoped>
  .list
    position absolute
    top: 1.58rem
    bottom:0
    right:0
    width:.4rem
    display flex
    flex-direction column
    justify-content center
    .item
      line-height .4rem
      text-align center
      color:$bgColor
</style>
