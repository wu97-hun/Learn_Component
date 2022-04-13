<template>
  <div>
    <home></home>
    <button @click="change">change</button>
  </div>
</template>

<script>
import Home from "./Home.vue";
import { computed } from "vue";
export default {
  components: {
    Home,
  },
  data() {
    return {
      names: ["w", "j", "l"],
    };
  },
  methods: {
    change() {
      this.names.push("m", "j");
    },
  },
  // provide: {
  //   name: "wj",
  //   woman: "lmj",
  // },
  // 对象形式的provide中的this指向的是script标签中的this，是undefined
  // 若需使用this则写函数形式
  provide() {
    return {
      name: "wj",
      woman: "lmj",
      // 响应式的
      length: computed(() => this.names.length), // computed返回的是ref对象，值在.value中
    };
  },
};
</script>

<style scoped>
</style>