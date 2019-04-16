<template>
  <div class="card" v-on:click="onClick">
    <img v-show="!isSelected" v-bind:src="beer.image_url">
    <div v-show="isSelected" class="description">
      <h3>Description</h3>
      <p>{{ beer.description }}</p>
    </div>
    <div class="container">
      <h4>
        <b>{{beer.name}}</b>
      </h4>
      <p>{{beer.tagline}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Beer",
  props: ["beer", "isSelected"],
  methods: {
    onClick() {
      this.$emit('beer-click', this.beer.id);
    }
  }
};
</script>

<style scoped>
.card:hover {
  box-shadow: 0 10px 10px 0 rgba(0, 0, 0, 0.5);
}

.card {
  color: black;
  transition: 0.3s;
  border-radius: 5px;
  width: 300px;
  height: 330px;
  margin: 20px;
  padding-top: 20px;
  background-color: rgba(235, 185, 93, 0.5);
}

img {
  width: 80px;
  height: 200px;
  border-radius: 5px;
}
.description {
  width: 260px;
  height: 206px;
  border-radius: 5px;
  overflow: scroll;
  margin: auto;
  text-align: justify;
}
</style>