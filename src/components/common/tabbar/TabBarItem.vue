<template>
  <div id="tab-bar-item" @click="itemClick">
    <div v-if="!isActive">
      <slot name="tab-icon"></slot>
    </div>
    <div v-else>
      <slot name="tab-icon-active"></slot>
    </div>
    <div :style="currenStyle">
      <slot name="tab-text"></slot>
    </div>
  </div>
</template>
<script>
export default {
  name: "VueEduTabbaritem",
  props: {
    path: String,
    currentColor: {
      type: String,
      default: "#ccc",
    },
  },
  data() {
    return {};
  },
  computed: {
    isActive() {
      return this.$route.path.indexOf(this.path) != -1;
    },
    currenStyle() {
      // console.log(this.isActive);
      return this.isActive ? { color: this.currentColor } : {};
    },
  },
  methods: {
    itemClick() {
      this.$router.replace(this.path);
    },
  },
};
</script>
<style  scoped>
#tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 10px;
}
#tab-bar-item img {
  width: 25px;
  height: 25px;
  margin-top: 5px;
  vertical-align: middle;
  margin-bottom: 4px;
}
</style>
