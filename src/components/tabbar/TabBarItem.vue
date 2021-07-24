<template>
  <div class="tab-item">
    <div v-if="!isActive">
      <slot name="img"> </slot>
    </div>
    <div v-else>
      <slot name="imgActive"> </slot>
    </div>
    <div :class="{ active: isActive }">
      <slot name="title"></slot>
    </div>
  </div>
</template>
<script>
export default {
  name: "",
  data() {
    return {
      isActive: false,
    };
  },
};
</script>
<style lang="scss">
.tab-item {
  flex: 1;
  flex-direction: column;
  align-items: center;
  height: 49px;
  background-color: #eee;
  display: flex;
  justify-content: center;
  font-size: 0.8rem;
  img {
    width: 25%;
    margin: 2px 0;
    object-fit: contain;
  }

  .active {
    color: #f54242;
  }
}
</style>
