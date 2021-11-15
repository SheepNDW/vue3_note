<template>
  <Demo @hello="showHelloMsg" msg="你好阿" school="特雷森">
    <template v-slot:qwe>
      <span>AAAAAA</span>
    </template>
  </Demo>
</template>

<script>
import Demo from "./components/Demo.vue";
export default {
  name: "App",
  components: { Demo },
  setup() {
    function showHelloMsg(value) {
      alert(`你好阿, 你觸發了hello事件, 我收到的參數是:${value}!`);
    }

    return {
      showHelloMsg,
    };
  },
};
</script>
