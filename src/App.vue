<template>
  <div id="app">
    <tab-bar>
      <tab-bar-item>
        <template v-slot:img>
          <img src="../src/assets/img/tabbar/home.png" alt="" />
        </template>
        <template v-slot:imgActive>
          <img src="../src/assets/img/tabbar/home-active.svg" alt="" />
        </template>
        <template v-slot:title> <div>首頁</div> </template>
      </tab-bar-item>

      <tab-bar-item>
        <template v-slot:img>
          <img src="../src/assets/img/tabbar/shopping-bag.png" alt="" />
        </template>
        <template v-slot:imgActive>
          <img src="../src/assets/img/tabbar/shopping-bag-active.svg" alt="" />
        </template>
        <template v-slot:title>
          <div>分類</div>
        </template>
      </tab-bar-item>

      <tab-bar-item>
        <template v-slot:img>
          <img src="../src/assets/img/tabbar/shopping-cart.png" alt="" />
        </template>
        <template v-slot:imgActive>
          <img src="../src/assets/img/tabbar/cart-active.svg" alt="" />
        </template>
        <template v-slot:title>
          <div>購物車</div>
        </template>
      </tab-bar-item>

      <tab-bar-item>
        <template v-slot:img>
          <img src="../src/assets/img/tabbar/user.png" alt="" />
        </template>
        <template v-slot:imgActive>
          <img src="../src/assets/img/tabbar/user-active.png" alt="" />
        </template>
        <template v-slot:title> <div>我的</div> </template>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>

<script>
import TabBar from "./components/tabbar/TabBar.vue";
import TabBarItem from "./components/tabbar/TabBarItem.vue";
export default {
  name: "App",
  components: {
    TabBar,
    TabBarItem,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/all.scss";
</style>
