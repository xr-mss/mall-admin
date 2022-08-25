<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>
<script>
import Layout from "./views/Layout.vue";
export default {
  name: "VueApp",
  data() {
    return {};
  },

  mounted() {},

  methods: {},
  components: {
    Layout,
  },
};
</script>
<style lang="less"></style>
