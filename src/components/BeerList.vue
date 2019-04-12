<template>
  <div class="main">
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
    <Beer/>
  </div>
</template>

<script>
import Beer from "./Beer.vue";

export default {
  name: "BeerList",
  components: {
    Beer
  }
};
</script>
<style scoped>
.main {
  width: 100%;
  display: flex;
  overflow: scroll;
  flex-wrap: wrap;
  justify-content: space-between;
}
</style>


