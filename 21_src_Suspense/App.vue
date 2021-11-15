<template>
  <div class="app">
    <h3>我是App組件</h3>
    <Suspense>
      <template v-slot:default>
        <Child />
      </template>
      <template v-slot:fallback>
        <h3>加載中...請稍等...</h3>
      </template>
    </Suspense>
  </div>
</template>

<script>
// import Child from "./components/Child.vue"; // 靜態引入
import { defineAsyncComponent } from "vue";
const Child = defineAsyncComponent(() => import("./components/Child.vue")); // 異步引入
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
