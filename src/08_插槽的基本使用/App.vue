<template>
  <div>
    <my-slot-cpn>
      <button>btn</button>
    </my-slot-cpn>
    <my-slot-cpn>
      <my-button></my-button>
    </my-slot-cpn>
    <my-slot-cpn>
      <h1>hhh</h1>
      <h1>xxx</h1>
    </my-slot-cpn>
    <my-slot-cpn />
  </div>
</template>

<script>
import MyButton from "./MyButton.vue";
import MySlotCpn from "./MySlotCpn.vue";
export default {
  components: {
    MySlotCpn,
    MyButton,
  },
};
</script>

<style scoped>
</style>