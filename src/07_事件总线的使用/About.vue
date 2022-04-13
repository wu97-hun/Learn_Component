<template>
  <div>
    <button @click="btnClick">click</button>
  </div>
</template>

<script>
import emitter from "./utils/eventBus";
export default {
  methods: {
    btnClick() {
      console.log("btnClick");
      emitter.emit("wj", { name: "wj", age: 25 });
      // emitter.emit("lmj", { name: "lmj", age: 25 });
    },
  },
};
</script>

<style scoped>
</style>