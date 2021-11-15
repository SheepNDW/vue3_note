<template>
  <h1>一個人的信息</h1>
  <h2>姓名: {{ person.name }}</h2>
  <h2>年齡: {{ person.age }}</h2>
  <h3>工作種類: {{ person.job.type }}</h3>
  <h3>工作薪資: {{ person.job.salary }}</h3>
  <h3>愛好: {{ person.hobby }}</h3>
  <h3>測試的數據c: {{ person.job.a.b.c }}</h3>
  <button @click="changeInfo">更改個人信息</button>
</template>

<script>
import { reactive } from "vue";
export default {
  name: "App",
  // 此處只是測試一下setup 暫時不考慮響應式
  setup() {
    // 數據
    let person = reactive({
      name: "張三",
      age: 18,
      job: {
        type: "前端工程師",
        salary: "30k",
        a: {
          b: {
            c: 666,
          },
        },
      },
      hobby: ["抽菸", "喝酒", "燙頭"],
    });

    // 方法
    function changeInfo() {
      person.name = "李四";
      person.age = 48;
      person.job.type = "UI設計師";
      person.job.salary = "60k";
      person.job.a.b.c = 999;
      person.hobby[0] = "學習";
    }

    // 返回一個對象 (常用)
    return {
      person,
      changeInfo,
    };
  },
};
</script>

<style></style>
