<template>
<TabBar>
    <TabBarItem path="/home"  activecolor="red">
      <div slot="item-icon"><img src="~assets/img/tabbar/icon01.png" alt=""></div>
      <div slot="item-icon-active"><img src="~assets/img/tabbar/icon01_active.png" alt=""></div>
      <div slot="item-text">首页</div>
    </TabBarItem>

    <TabBarItem path="/category"  activecolor="green">
      <div slot="item-icon"><img src="~assets/img/tabbar/icon02.png" alt=""></div>
      <div slot="item-icon-active"><img src="~assets/img/tabbar/icon02_active.png" alt=""></div>
      <div slot="item-text">分类</div>
    </TabBarItem>

    <TabBarItem path="/cart" activecolor="deeppink">
      <div slot="item-icon"><img src="~assets/img/tabbar/icon03.png" alt=""></div>
      <div slot="item-icon-active"><img src="~assets/img/tabbar/icon03_active.png" alt=""></div>
      <div slot="item-text">购物车</div>
    </TabBarItem>

    <TabBarItem path="/profile" activecolor="blue">
      <div slot="item-icon"><img src="~assets/img/tabbar/icon04.png" alt=""></div>
      <div slot="item-icon-active"><img src="~assets/img/tabbar/icon04_active.png" alt=""></div>
      <div slot="item-text">我的</div>
    </TabBarItem>
  </TabBar>
</template>

<script>
import TabBar from "../common/tabbar/TabBar";
import TabBarItem from "../common/tabbar/TabBarItem";

export default {
  name: "Maintabbar",
  components:{
     TabBar,TabBarItem
  }
}
</script>

<style scoped>
@import "~assets/css/normalize.css";
@import "~assets/css/base.css";
</style>
