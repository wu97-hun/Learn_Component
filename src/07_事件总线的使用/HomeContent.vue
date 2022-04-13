<template>
  <div></div>
</template>

<script>
import emitter from "./utils/eventBus";
export default {
  created() {
    emitter.on("wj", (info) => {
      console.log("wj:", info);
    });
    emitter.on("lmj", (info) => {
      console.log("lmj:", info);
    });
    // 监听所有事件
    emitter.on("*", (type, info) => {
      // type就是事件的名称
      console.log("* listenr:", type, info);
    });
  },
};
</script>

<style scoped>
</style>