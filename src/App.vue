<template>
  <div class="app">
    <div class="a1">
      <router-link to="/">首页 </router-link>
      <router-link to="/about">写作 </router-link>
      <router-link to="/aaa">关于...</router-link>
    </div>
    <br />
    <br />
    <router-view />
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style>
.app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  height: 80px;
  text-decoration: none;
}
a {
  text-decoration: none;

  color: rgb(101, 165, 218);
}
a:hover {
  font-size: 20px;
  font-weight: 500;
}
</style>
