<template>
  <div id="app">
    <Navbar/>
    <BeerList/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import BeerList from './components/BeerList.vue'

export default {
  name: 'app',
  components: {
    Navbar,
    BeerList
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  margin: 0;
}
</style>
