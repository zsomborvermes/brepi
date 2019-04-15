<template>
  <div class="paginator">
    <button v-show="pageNumber > 1" v-on:click="changePage(pageNumber - 1)"><<</button>
    <button v-show="pageNumber > 1" v-on:click="changePage(1)">First</button>
    <button v-show="pageNumber > 2" v-on:click="changePage(pageNumber - 2)">{{pageNumber - 2}}</button>
    <button v-show="pageNumber > 1" v-on:click="changePage(pageNumber - 1)">{{pageNumber - 1}}</button>
    <button class="current-page">{{pageNumber}}</button>
    <button v-on:click="changePage(pageNumber + 1)">{{pageNumber + 1}}</button>
    <button v-on:click="changePage(pageNumber + 2)">{{pageNumber + 2}}</button>
    <button v-on:click="changePage(pageNumber + 1)">>></button>
  </div>
</template>
<script>
export default {
  name: 'Paginator',
  data() {
    return {
      pageNumber: 1
    }
  },
  methods: {
    changePage(pageNumber) {
      this.pageNumber = pageNumber;
      this.$emit('change-page', pageNumber);
    }
  }
};
</script>
<style scoped>
.paginator {
  display: flex;
  justify-content:center;
}

button {
  font-size: 15px;
  height: 40px;
  width: 40px;
  background-color: transparent;
  border: 0;
}

button:hover {
  background-color:  rgba(0, 0, 0, 0.2);
  border-radius: 20px;
}

.current-page {
  font-size: 20px;
  font-weight: bold;
}
</style>


