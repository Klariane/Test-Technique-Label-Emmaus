<template>
  <div class="carousel">
    <slot></slot>
    <button class="carousel__nav carousel__next" @click.prevent="next"></button>
    <button class="carousel__nav carousel__prev" @click.prevent="prev"></button>
  </div>
</template>
<script>
export default {
  data () {
    return {
      index: 0,
      slides: []
    }
  },
  mounted () {
    this.slides = this.$children
    this.slides.forEach((slide, i) => {
      slide.index = i
    })
  },
  computed: {
    slidesCount () {
      return this.slides.length
    }
  },
  methods: {
    next () {
      this.index++
      if (this.index >= this.slidesCount) {
        this.index = 0
      }
    },
    prev () {
      this.index--
      if (this.index < 0) {
        this.index = this.slidesCount - 1
      }
    }
  }
}
</script>
<style>
.carousel {
  position: relative;
}
.carousel__nav.carousel__prev{
  position:absolute;
  top:70%;
  margin-top: 30px;
  left: 1300px;
  background-image: url(chevron-right-solid.svg);
  height: 50px;
  width: 63px;

}
.carousel__nav.carousel__next{
  position:absolute;
  right: 10px;
  top:70%;
  left: 10px;
  background-image: url(chevron-left-solid.svg);
  height: 50px;
  width: 63px;
}

</style>
