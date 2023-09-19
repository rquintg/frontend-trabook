<template>
  <div id="app">
    <NavBar />
    <BannerContent />
    <CardsUtil />
  </div>
</template>

<script>

import NavBar from './components/NavBar.vue'
import BannerContent from './components/BannerContent.vue'
import CardsUtil from './components/CardsUtil.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    BannerContent,
    CardsUtil
  }
}
</script>

<style>
#app {
  /*font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;*/
}
</style>
