<template>
  <tab-bar>
    <template v-slot:items>
      <!-- 也可以傳active-color來改變字的顏色(傳props到TabBarItem.vue) 否則就用預設的#f54242 -->
      <tab-bar-item path="/home" active-color="#f40">
        <template v-slot:img>
          <img src="../../assets/img/tabbar/home.png" alt="" />
        </template>
        <template v-slot:imgActive>
          <img src="../../assets/img/tabbar/home-active.svg" alt="" />
        </template>
        <template v-slot:title> <div>首頁</div> </template>
      </tab-bar-item>

      <tab-bar-item path="/category">
        <template v-slot:img>
          <img src="../../assets/img/tabbar/shopping-bag.png" alt="" />
        </template>
        <template v-slot:imgActive>
          <img src="../../assets/img/tabbar/shopping-bag-active.svg" alt="" />
        </template>
        <template v-slot:title>
          <div>分類</div>
        </template>
      </tab-bar-item>

      <tab-bar-item path="/cart">
        <template v-slot:img>
          <img src="../../assets/img/tabbar/shopping-cart.png" alt="" />
        </template>
        <template v-slot:imgActive>
          <img src="../../assets/img/tabbar/cart-active.svg" alt="" />
        </template>
        <template v-slot:title>
          <div>購物車</div>
        </template>
      </tab-bar-item>

      <tab-bar-item path="/mine">
        <template v-slot:img>
          <img src="../../assets/img/tabbar/user.png" alt="" />
        </template>
        <template v-slot:imgActive>
          <img src="../../assets/img/tabbar/user-active.png" alt="" />
        </template>
        <template v-slot:title> <div>我的</div> </template>
      </tab-bar-item>
    </template>
  </tab-bar>
</template>
<script>
import TabBar from "./TabBar.vue";
import TabBarItem from "./TabBarItem.vue";

export default {
  name: "",
  data() {
    return {};
  },
  components: {
    TabBar,
    TabBarItem,
  },
};
</script>
<style lang="scss"></style>
