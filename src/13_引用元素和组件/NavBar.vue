<template>
  <div>
    <h2>NavBar组件</h2>
    <button @click="getParentAndRoot">获取父组件和根组件</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: "hello",
    };
  },
  methods: {
    getParentAndRoot() {
      console.log(this.$parent, this.$root);
    },
  },
};
</script>

<style scoped>
</style>