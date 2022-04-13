<template>
  <div>
    <button @click="increment">+1</button>
    <button @click="decrement">-1</button>
    <input type="text" v-model.number="num" />
    <button @click="incrementN">+n</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 0,
    };
  },
  // emits包含所有触发的事件，若需要验证参数则使用对象写法
  // emits: ["add", "sub", "addN"]
  emits: {
    add: null,
    sub: null,
    addN(payload, man, woman) {
      console.log(payload, man, woman);
      if (payload > 10) {
        return true;
      }
      return false;
    },
  },
  methods: {
    increment() {
      console.log("+1");
      this.$emit("add");
    },
    decrement() {
      console.log("-1");
      this.$emit("sub");
    },
    incrementN() {
      this.$emit("addN", this.num, "wj", "lmj");
    },
  },
};
</script>

<style scoped>
</style>