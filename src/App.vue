<template>
  <Navbar/>
  <Intro/>
  <Hours/>
  <Map/>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Map from './components/Map.vue'

import Intro from './sections/Intro.vue'
import Hours from './sections/Hours.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Map,
    Intro,
    Hours
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
