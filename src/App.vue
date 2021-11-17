<template>
  <div id="app">
    <Menu></Menu>
    <Carousel></Carousel>
    <Card1></Card1>
    <card2></card2>

  </div>
</template>

<script>
import Menu from './components/Menu.vue'
import Carousel from './components/Carousel.vue'
import Card1 from './components/Card1.vue'
import card2 from './components/card2.vue'

export default {
  name: 'App',
  components: {
    Menu,
    Carousel,
    Card1,
    card2
  }
}
</script>
