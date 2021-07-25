<template>
  <div id="app">
    <router-view></router-view>
    <main-tab-bar></main-tab-bar>
  </div>
</template>

<script>
import MainTabBar from "./components/tabbar/MainTabBar.vue";

export default {
  components: { MainTabBar },
  name: "App",
  components: {
    MainTabBar,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/all.scss";
</style>
