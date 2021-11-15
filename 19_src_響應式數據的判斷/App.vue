<template>
  <h3>我是App組件</h3>
</template>

<script>
import {
  ref,
  reactive,
  readonly,
  toRefs,
  isRef,
  isReactive,
  isReadonly,
  isProxy,
} from "vue";
export default {
  name: "App",
  setup() {
    let car = reactive({ name: "奔馳", price: "40W" });
    let sum = ref(0);
    let car2 = readonly(car);

    console.log(isRef(sum));
    console.log(isReactive(car));
    console.log(isReadonly(car2));
    console.log(isProxy(car));
    console.log(isProxy(sum));

    return { ...toRefs(car) };
  },
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
