<template>
  <nav>
    <a class="nav-text" href="/">brepi</a>
    <div class="nav-options">
      <a href="/">Home</a>
      <a href="#">About</a>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar"
};
</script>
<style scoped>
nav {
  background-color: rgba(150, 79, 12, 0.9);
  height: 80px;
}

.nav-text {
  color: yellow;
  font-size: 40px;
  float: left;
  margin: 10px;
}

.nav-options {
  font-size: 30px;
  float: right;
  margin: 20px;
}

a {
  text-decoration: none;
  color: black;
  margin-right: 40px;
}
a:hover {
  color: yellow;
}
</style>



