<template>
  <div class="tab-bar">
    <slot name="items"></slot>
  </div>
</template>
<script>
export default {
  name: "",
  data() {
    return {};
  },
  components: {},
};
</script>
<style lang="scss">
.tab-bar {
  display: flex;
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  box-shadow: 0px -1px 1px rgba(196, 196, 196, 0.4);
}
</style>
