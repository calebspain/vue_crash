<template>
  <header class="header">
    <h1>TodoList</h1>
    <div id="nav">
      <router-link to="/">Home</router-link>|
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
.header {
  padding: 10px;
  text-align: center;
  color: #fff;
  background: #333;
}

.header > #nav > a {
  padding-right: 5px;
  color: #fff;
  text-decoration: none;
}
</style>