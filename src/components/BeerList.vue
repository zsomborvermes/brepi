<template>
  <div>
    <div class="main">
      <div v-bind:key="beer.id" v-for="beer in beerList">
        <Beer
          v-on:beer-click="handleClick"
          v-bind:isSelected="selectedBeerId === beer.id"
          v-bind:beer="beer"
        />
      </div>
    </div>
    <Paginator v-on:change-page="changePage"/>
  </div>
</template>

<script>
import Beer from "./Beer.vue";
import Paginator from "./Paginator.vue";

export default {
  name: "BeerList",
  components: {
    Beer,
    Paginator
  },
  data() {
    return {
      selectedBeerId: 0
    };
  },
  props: ["beerList"],
  methods: {
    handleClick(id) {
      if (this.selectedBeerId === id) {
        this.selectedBeerId = 0;
      } else {
        this.selectedBeerId = id;
      }
    },
    changePage(pageNumber) {
      this.$emit("change-page", pageNumber);
    }
  }
};
</script>
<style scoped>
.main {
  width: 100%;
  display: flex;
  overflow: scroll;
  flex-wrap: wrap;
  justify-content: center;
}
</style>


