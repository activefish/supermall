<template>
  <tab-bar>
    <tab-bar-item path="/home" currentColor="red">
      <img src="~assets/img/tabbar/home.png" slot="tab-icon" />
      <img src="~assets/img/tabbar/home-active.png" slot="tab-icon-active" />
      <div slot="tab-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category" currentColor="red">
      <img src="~assets/img/tabbar/shopping.png" slot="tab-icon" />
      <img src="~assets/img/tabbar/shopping-active.png" slot="tab-icon-active" />
      <div slot="tab-text">种类</div>
    </tab-bar-item>
    <tab-bar-item path="/list" currentColor="red">
      <img src="~assets/img/tabbar/list.png" slot="tab-icon" />
      <img src="~assets/img/tabbar/list-active.png" slot="tab-icon-active" />
      <div slot="tab-text">列表</div>
    </tab-bar-item>
    <tab-bar-item path="/profile" currentColor="red">
      <img src="~assets/img/tabbar/me.png" slot="tab-icon" />
      <img src="~assets/img/tabbar/me-active.png" slot="tab-icon-active" />
      <div slot="tab-text">我的</div>
    </tab-bar-item>
  </tab-bar>
</template>
<script>
import TabBar from "components/common/tabbar/TabBar";
import TabBarItem from "components/common/tabbar/TabBarItem";

export default {
  name: "VueEduMaintabbar",
  components: {
    TabBar,
    TabBarItem,
  },
  data() {
    return {};
  },
};
</script>
<style  scoped>
</style>
