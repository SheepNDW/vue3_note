<template>
  <div class="app">
    <h3>我是App組件</h3>
    <Child />
  </div>
</template>

<script>
import Child from "./components/Child.vue";
export default {
  name: "App",
  components: { Child },
};
</script>

<style>
* {
  font-family: 微軟正黑體;
}
.app {
  background-color: gray;
  padding: 10px;
}
</style>
