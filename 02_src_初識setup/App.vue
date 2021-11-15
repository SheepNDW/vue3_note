<template>
  <h1>一個人的信息</h1>
  <h2>姓名: {{ name }}</h2>
  <h2>年齡: {{ age }}</h2>
  <button @click="sayHello">說話</button>
</template>

<script>
// import { h } from "vue";
export default {
  name: "App",
  // 此處只是測試一下setup 暫時不考慮響應式
  setup() {
    // 數據
    let name = "張三";
    let age = 18;

    // 方法
    function sayHello() {
      alert(`我叫${name} 我${age}歲了, 你好阿!`);
    }

    // 返回一個對象 (常用)
    return {
      name,
      age,
      sayHello,
    };

    // 返回一個函數 (渲染函數)
    // return () => h("h1", "尚硅谷");
  },
};
</script>

<style></style>
