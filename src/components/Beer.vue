<template>
  <div class="card">
    <img
      src="https://cdn.shopify.com/s/files/1/0810/4433/products/beer_gold_b228a9f0-c006-4059-8135-53ab896fe9f1_large.jpg?v=1527636163"
    >
    <div class="container">
      <h4>
        <b>Beer</b>
      </h4>
      <p>Delicious!</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Beer"
};
</script>

<style scoped>
.card:hover {
  box-shadow: 0 10px 20px 0 rgba(0, 0, 0, 0.5);
}

.card {
  transition: 0.3s;
  border-radius: 5px;
  width: 300px;
  height: 330px;
  margin: 20px;
  background-color: lightcoral;
}

img {
  margin-top: 20px;
  width: 200px;
  height: 200px;
  border-radius: 5px;
}
</style>