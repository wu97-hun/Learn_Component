<template>
  <div>
    <tab-contral :product-list="productList" @clickItem="toggle"></tab-contral>
    <h1>{{ contents[currentIndex] }}</h1>
  </div>
</template>

<script>
import TabContral from "./TabContral.vue";
export default {
  components: {
    TabContral,
  },
  data() {
    return {
      currentIndex: 0,
      productList: ["衣装", "娱乐", "吃喝"],
      contents: ["衣装界面", "娱乐界面", "吃喝界面"],
    };
  },
  methods: {
    toggle(index) {
      this.currentIndex = index;
    },
  },
};
</script>

<style scoped>
</style>