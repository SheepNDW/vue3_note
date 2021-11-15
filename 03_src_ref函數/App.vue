<template>
  <h1>一個人的信息</h1>
  <h2>姓名: {{ name }}</h2>
  <h2>年齡: {{ age }}</h2>
  <h3>工作種類: {{ job.type }}</h3>
  <h3>工作薪資: {{ job.salary }}</h3>
  <button @click="changeInfo">更改個人信息</button>
</template>

<script>
import { ref } from "vue";
export default {
  name: "App",
  // 此處只是測試一下setup 暫時不考慮響應式
  setup() {
    // 數據
    let name = ref("張三");
    let age = ref(18);
    let job = ref({
      type: "前端工程師",
      salary: "30k",
    });

    // 方法
    function changeInfo() {
      (name.value = "李四"), (age.value = 48);
      job.value.type = "UI設計師";
      job.value.salary = "60k";
    }

    // 返回一個對象 (常用)
    return {
      name,
      age,
      job,
      changeInfo,
    };
  },
};
</script>

<style></style>
