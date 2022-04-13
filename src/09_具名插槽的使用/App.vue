<template>
  <div>
    <nav-bar :name="name">
      <!-- 具名插槽，不带v-slot则会变为v-slot:default -->
      <!-- v-slot: 可换为 # -->
      <template #left>
        <button>left</button>
      </template>
      <template #center>
        <h2>title</h2>
      </template>
      <template #right>
        <i>right</i>
      </template>
      <!-- #[name] []代表取出data中的name -->
      <template #[name]>
        <i>wj</i>
      </template>
    </nav-bar>
  </div>
</template>

<script>
import NavBar from "./NavBar.vue";
export default {
  components: {
    NavBar,
  },
  data() {
    return {
      name: "wj",
    };
  },
};
</script>

<style scoped>
</style>