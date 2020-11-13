<template>
  <div class="a3">
    <h1>{{ biaoti }}</h1>
    <h4>{{ zhengwen }}</h4>
  </div>
</template>

<script>
export default {
  name: "blogs",
  props: ["zhengwen", "biaoti"]
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.a3 {
  display: -webkit-flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  width: 80%;
  margin: 0 auto;
}
h1 {
  color: #899bad;
}
h4 {
  color: #6b7b8d;
  text-align: left;
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>
