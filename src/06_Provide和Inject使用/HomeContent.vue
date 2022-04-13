<template>
  <div>
    <h1>{{ name + length.value + woman }}</h1>
  </div>
</template>

<script>
export default {
  inject: ["name", "woman", "length"],
};
</script>

<style scoped>
</style>