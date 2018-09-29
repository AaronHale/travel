<template>
    <div class="container" @click="handleGallaryClick">
      <div class="wrapper">
        <swiper :options="swiperOptions"><!-- slides 父组件传递swiperOptions给swiper子组件 -->
          <swiper-slide v-for="(item,index) of imags" :key="index">
            <img class="gallary-img" alt="" :src="item">
          </swiper-slide>
          <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
      </div>
    </div>

</template>

<script>
export default {
  name: 'CommonGallary',
  props: {
    imags: {
      Array,
      default () {
        return [
          'http://img1.qunarzz.com/sight/p0/1410/34/f540a04367d06820af4dfeaf0ad40257.water.jpg_r_800x800_479f9b55.jpg',
          'http://img1.qunarzz.com/wugc/p180/201306/16/7f08e81624346b1693835fbb.jpg_r_800x800_5f03ad73.jpg'
        ]
      }
    }
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        observeParents: true,
        observer: true
      }
    }
  },
  methods: {
    handleGallaryClick () {
      this.$emit('close')
    }
  }
}
</script>

<style lang="stylus" scoped>
  .container >>> .swiper-container
    overflow inherit
  .container
    display flex
    flex-direction column
    justify-content center
    z-index 99
    position fixed
    top 0
    bottom 0
    left 0
    right 0
    background #000
    .wrapper
      width 100%
      padding-bottom 100%
      height 0
      .gallary-img
        width 100%
      .swiper-pagination
        color #fff
        bottom: -4rem
</style>
