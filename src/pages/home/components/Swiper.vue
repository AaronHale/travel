<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper"><!-- slides 父组件传递swiperOptions给swiper子组件 -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img :src="item.imgUrl" alt="" class="swiper-img">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    swiperList: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 3000
      }
    }
  },
  computed: {
    showSwiper () {
      return this.swiperList.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff;
  .wrapper
    width:100%
    height:0
    overflow: hidden
    padding-bottom:31%  /*解决图片未加载时高度塌陷*/
    background: #fffffe
    .swiper-img
      width:100%
</style>
