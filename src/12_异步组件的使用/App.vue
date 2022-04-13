<template>
  <div>App组件</div>
  <home></home>
  <suspense>
    <template #default>
      <async-category></async-category>
    </template>
    <template #fallback>
      <loading></loading>
    </template>
  </suspense>
</template>

<script>
import { defineAsyncComponent } from "vue";
import Home from "./Home.vue";
import Loading from "./Loading.vue";
// import AsyncCategory from "./AsyncCategory.vue";
// import("./AsyncCategory.vue")返回的是一个promise对象
// defineAsyncComponent函数定义异步组件，单独打包
const AsyncCategory = defineAsyncComponent(() => import("./AsyncCategory.vue"));

// 异步组件对象写法
// const AsyncCategory = defineAsyncComponent({
//   loader: () => import("./AsyncCategory.vue"),
//   // 加载时显示的组件
//   loadingComponent: Loading,
//   // errorComponent（加载失败时显示的组件）
//   // 显示loadingComponent等待的时间
//   delay: 2000,
//   /*
//    * onError组件加载失败的函数
//    * err：错误信息
//    * retry：调用重新加载
//    * fail：一个函数，指示加载程序结束退出
//    * attempts：记录尝试的次数
//    */
//   onError: function (err, retry, fail, attempts) {},
// });

export default {
  components: {
    Home,
    AsyncCategory,
    Loading,
  },
};
</script>

<style scoped>
</style>