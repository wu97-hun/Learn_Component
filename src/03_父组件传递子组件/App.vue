<template>
  <div>
    <!-- class style id 都属于非prop的attribute -->
    <show-message
      id="lmj"
      class="wj"
      :title="titele"
      :message="message"
    ></show-message>
    <!-- v-bind直接传对象 牢记！ -->
    <show-message v-bind="info"></show-message>
    <multi-root-element id="aaa"></multi-root-element>
  </div>
</template>

<script>
import MultiRootElement from "./MultiRootElement.vue";
import ShowMessage from "./ShowMessage.vue";
export default {
  data() {
    return {
      titele: "hello props",
      message: "msg",
      info: {
        title: "hhhhh",
        message: "xxxxx",
      },
    };
  },
  components: {
    ShowMessage,
    MultiRootElement,
  },
};
</script>

<style scoped>
</style>