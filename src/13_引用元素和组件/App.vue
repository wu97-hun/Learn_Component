<template>
  <div>
    <h2 ref="myh2">hahaha</h2>
    <nav-bar ref="navBar"></nav-bar>
    <button @click="btnClick">get Element</button>
  </div>
</template>

<script>
import NavBar from "./NavBar.vue";
export default {
  name: "App",
  components: { NavBar },
  methods: {
    btnClick() {
      // console.log(this.$refs.myh2);
      console.log(this.$refs.navBar.msg);
    },
  },
};
</script>

<style scoped>
</style>