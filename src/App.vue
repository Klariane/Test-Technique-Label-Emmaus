<template>
  <div id="app">
    <Menu></Menu>
    <carousel>
      <carousel-slide>
        <div style="position:absolute; left:0; right:0; text-align:center; top:50%; color:#EDFCF8; font-size:16px;"></div>
       <a class="carousel__nav carousel__next" @click.prevent="next"><img src="./assets/Carousel1.png" alt="image1" width="100%"></a>
      </carousel-slide>
      <carousel-slide>
        <div style="position:absolute; left:0; right:0; text-align:center; top:50%; color:#EDFCF8; font-size:16px;"></div>
        <img src="./assets/Carousel2.png" alt="Image2" width="100%">
      </carousel-slide>
      <carousel-slide>
        <div style="position:absolute; left:0; right:0; text-align:center; top:50%; color:#EDFCF8; font-size:16px;"></div>
        <img src="./assets/Carousel3.png" alt="Image3" width="100%">
      </carousel-slide>
    </carousel>

  </div>
</template>

<script>
import Menu from './components/Menu.vue'
import Carousel from './components/carousel/Carousel.vue'
import CarouselSlide from './components/carousel/CarouselSlide.vue'

export default {
  name: 'App',
  components: {
    Menu,
    Carousel,
    CarouselSlide
  },
  data () {
    return {
      index: 0,
      slides: []
    }
  }
}
</script>
