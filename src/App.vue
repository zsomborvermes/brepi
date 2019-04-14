<template>
  <div id="app">
    <Navbar/>
    <BeerList v-on:change-page="changePage" v-bind:beerList="this.beerList"/>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import BeerList from "./components/BeerList.vue";

export default {
  name: "app",
  components: {
    Navbar,
    BeerList
  },
  data() {
    return {
      beerList: []
    };
  },
  methods: {
    changePage(pageNumber) {
      fetch(`https://api.punkapi.com/v2/beers?page=${pageNumber}&per_page=8`)
        .then(res => res.json().then(data => (this.beerList = data)))
        .catch(err => console.log(err));
    }
  },
  created() {
    fetch(`https://api.punkapi.com/v2/beers?page=1&per_page=8`)
      .then(res => res.json().then(data => (this.beerList = data)))
      .catch(err => console.log(err));
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  margin: 0;
  height: 100vh;
  background-image: url("https://ak4.picdn.net/shutterstock/videos/1426564/thumb/3.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
