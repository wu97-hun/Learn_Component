<template>
  <div>
    <input type="text" v-model="value" />
    <input v-model="wj" />
  </div>
</template>

<script>
export default {
  props: {
    msg: String,
    modelValue: String,
  },
  emits: ["update:msg", "update:modelValue"],
  computed: {
    value: {
      get() {
        return this.msg;
      },
      set(value) {
        this.$emit("update:msg", value);
      },
    },
    wj: {
      set(value) {
        this.$emit("update:modelValue", value);
      },
      get() {
        return this.modelValue;
      },
    },
  },
};
</script>

<style scoped>
</style>