<template>
  <div>
    <!-- $attrs包含传过来的所有非prop的attributes -->
    <h2 v-bind="$attrs">{{ title }}</h2>
    <h2>{{ message }}</h2>
  </div>
</template>

<script>
export default {
  // 禁用继承非prop的attribute
  inheritAttrs: false,
  // props: ["title", "message"],
  props: {
    title: String,
    message: {
      type: String,
      required: true,
      default: "qqqqq",
    },
  },
};
</script>

<style scoped>
</style>