<template>
<div class="tab-bar-item" @click="itemclick" >
      <div v-if="!IsActive"><slot name="item-icon"></slot></div>
      <div v-else><slot name="item-icon-active"></slot></div>
      <div :style="activestyle" ><slot name="item-text"></slot></div>
</div>
</template>

<script>
export default {
  name: "TabBarItem",
  props: {
   path: String,
    activecolor: {
    type: String,
    default: 'red'
   }
  },
  data(){ return {

    }
  },
  computed: {
    IsActive() {
      return this.$route.path.includes(this.path);
    },
    activestyle() {
      return this.IsActive ? {color:this.activecolor}:{}
    }
  },
  methods: {
    itemclick() {
        //this.$router.replace(this.path); 重复点击菜单报错
        this.$router.replace(this.path).catch(err => err);//解决
    },


  }
}
</script>

<style scoped>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}
.tab-bar-item img {
  width: 24px;
  height: 24px;
  /*margin-bottom: 2px;*/
  vertical-align: middle;
}

</style>
