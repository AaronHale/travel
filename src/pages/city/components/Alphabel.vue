<template>
    <ul class="list">
      <li
        class="item"
        v-for="item of letters"
        :key="item"
        :ref="item"
        @click="handleLetterClick"
        @touchstart="handleTouchStart"
        @touchmove="handleTouchMove"
        @touchend="handleTouchEnd"
      >
        {{item}}
      </li>
    </ul>
</template>

<script>
export default {
  name: 'CityAlphabel',
  props: {
    cities: Object
  },
  data () {
    return {
      touchStatus: false
    }
  },
  computed: {
    letters () {
      const letters = []
      for (let i in this.cities) {
        letters.push(i)
      }
      return letters
    }
  },
  methods: {
    handleLetterClick (e) {
      this.$emit('change', e.target.innerText)
    },
    handleTouchStart () {
      this.touchStatus = true
    },
    handleTouchMove (e) {
      if (this.touchStatus) {
        const startY = this.$refs['A'][0].offsetTop
        const touchY = e.touches[0].clientY - 79
        const index = Math.floor((touchY - startY) / 20)
        if (index >= 0 && index < this.letters.length) {
          this.$emit('change', this.letters[index])
        }
      }
    },
    handleTouchEnd () {
      this.touchStatus = false
    }
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
