<template>
    <ul class="list">
      <li class="item" v-for="(item,key) of cities" :key="key">{{key}}</li>
    </ul>
</template>

<script>
export default {
  name: 'CityAlphabel',
  props: {
    cities: Object
  }
}
</script>

<style lang="stylus" scoped>
  .list
    position absolute
    top:1.58rem
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
