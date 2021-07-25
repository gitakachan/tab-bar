<template>
  <div class="tab-item" @click="itemClick">
    <div v-if="!isActive">
      <slot name="img"> </slot>
    </div>
    <div v-else>
      <slot name="imgActive"> </slot>
    </div>
    <div :style="activeStyle">
      <slot name="title"></slot>
    </div>
  </div>
</template>
<script>
export default {
  name: "",
  props: {
    path: String,
    activeColor: {
      type: String,
      default: "#f54242",
    },
  },
  data() {
    return {
      // isActive: false,
    };
  },
  computed: {
    isActive() {
      //看當前處於活躍的路由path是否包含當前組件的path
      //{path:"/home"} vs. this.path ?
      return this.$route.path.indexOf(this.path) !== -1;
    },
    //綁定style 處於活躍則添加props傳進來的activeColor
    //但這裡活躍的圖片是紅色，字改成其他顏色很怪，所以就不要傳activeColor，然後使用預設值就好
    activeStyle() {
      return this.isActive ? { color: this.activeColor } : {};
    },
  },
  methods: {
    itemClick() {
      //console.log(this.path);
      this.isActive;
      this.$router.push(this.path);
    },
  },
};
</script>
<style lang="scss">
.tab-item {
  flex: 1;
  flex-direction: column;
  // height: 49px;
  padding: 5px 0;
  background-color: #eee;
  display: flex;
  justify-content: center;
  font-size: 0.8rem;
  text-align: center;

  img {
    width: 25%;
    margin: 2px 0;
    object-fit: contain;
  }
}
</style>
