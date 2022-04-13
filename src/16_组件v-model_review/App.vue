<template>
  <div>
    <wj-input v-model:msg="msg" v-model="title"></wj-input>
    {{ msg }}
    {{ title }}
  </div>
</template>

<script>
import WjInput from "./WjInput.vue";
export default {
  components: { WjInput },
  data() {
    return {
      msg: "",
      title: "",
    };
  },
};
</script>


    WjInput<style scoped>
</style>