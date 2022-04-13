<template>
  <div>
    <button
      :class="{ active: currentTab == item }"
      v-for="item in tabs"
      :key="item"
      @click="clickItem(item)"
    >
      {{ item }}
    </button>
    <keep-alive include="about">
      <component
        :is="currentTab"
        name="wj"
        :age="25"
        @pageClick="handle"
      ></component>
    </keep-alive>
 
    <!-- v-if实现 -->
    <!-- <template v-if="currentTab == 'home'">
      <home></home>
    </template>
    <template v-else-if="currentTab == 'about'">
      <about></about>
    </template>
    <template v-else>
      <category></category>
    </template> -->
  </div>
</template>

<script>
import About from "./pages/About.vue";
import Category from "./pages/Category.vue";
import Home from "./pages/Home.vue";
export default {
  components: {
    Home,
    About,
    Category,
  },
  data() {
    return {
      tabs: ["home", "about", "category"],
      currentTab: "home",
    };
  },
  methods: {
    clickItem(item) {
      if (item == this.currentTab) return;
      this.currentTab = item;
    },
    handle(info) {
      console.log(info);
    },
  },
};
</script>

<style scoped>
.active {
  color: salmon;
}
</style>