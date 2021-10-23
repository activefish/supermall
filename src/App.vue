<template>
  <div id="app">
    <router-view />
    <main-tab-bar />
  </div>
</template>
<script>
import MainTabBar from "components/content/tabbar/MainTabBar";
export default {
  name: "VueEduApp",
  components: { MainTabBar },
  data() {
    return {};
  },
};
</script>
<style>
@import "assets/css/normal.css";
</style>
