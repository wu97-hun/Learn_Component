<template>
  <div @click="divClick">Home组件 - {{ name }}</div>
</template>

<script>
export default {
  name: "home",
  props: {
    name: String,
    age: Number,
  },
  emits: ["pageClick"],
  methods: {
    divClick() {
      this.$emit("pageClick", "home");
    },
  },
};
</script>

<style scoped>
</style>