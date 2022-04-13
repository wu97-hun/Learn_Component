<template>
  <div>
    <child-cpn></child-cpn>
    <show-names :names="names">
      <!-- 若还需使用具名插槽则 v-slot:name="slotProps" -->
      <template v-slot:default="slotProps">
        <button>{{ slotProps.item }} - {{ slotProps.index }}</button>
      </template>
    </show-names>
    <!-- 默认插槽可以下简写（独占默认插槽的缩写） -->
    <show-names :names="names" v-slot="slotProps">
      <i>{{ slotProps.item }} - {{ slotProps.index }}</i>
    </show-names>
  </div>
</template>

<script>
import ChildCpn from "./ChildCpn.vue";
import ShowNames from "./ShowNames.vue";
export default {
  components: {
    ChildCpn,
    ShowNames,
  },
  data() {
    return {
      names: ["w", "j", "l", "m", "j"],
    };
  },
};
</script>

<style scoped>
</style>