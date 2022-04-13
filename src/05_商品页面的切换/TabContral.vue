<template>
  <div class="tab-control">
    <div
      class="tab-control-item"
      v-for="(item, index) in productList"
      :key="item"
      @click="clickCurrent(index)"
    >
      <span :class="{ active: currentIndex == index }">{{ item }}</span>
    </div>
  </div>
</template>

<script>
export default {
  emits: ["clickItem"],
  props: {
    productList: Array,
  },
  data() {
    return {
      currentIndex: 0,
    };
  },
  methods: {
    clickCurrent(index) {
      if (this.currentIndex == index) return;
      this.currentIndex = index;
      this.$emit("clickItem", index);
    },
  },
};
</script>

<style scoped>
.tab-control {
  display: flex;
}
.tab-control-item {
  flex: 1;
  text-align: center;
}
.tab-control-item .active {
  color: salmon;
  padding: 5px 5px;
  border-bottom: 2px solid salmon;
}
</style>