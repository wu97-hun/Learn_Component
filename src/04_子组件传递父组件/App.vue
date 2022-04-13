<template>
  <div>
    <h2>当前计数：{{ counter }}</h2>
    <counter-operation
      @add="counter++"
      @sub="counter--"
      @addN="counterAddN"
    ></counter-operation>
  </div>
</template>

<script>
import CounterOperation from "./CounterOperation.vue";
export default {
  components: {
    CounterOperation,
  },
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    // 此出的形参即为$emit传递来的参数
    counterAddN(num, man, woman) {
      console.log(man, woman);
      this.counter += num;
    },
  },
};
</script>

<style scoped>
</style>