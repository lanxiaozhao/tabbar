<!-- TabBarItem -->
<template>
<div class="tab-bar-item" @click="itemClick">
  <div v-if="isActive"><slot name="icon" ></slot></div>
  <div v-else><slot name="icon-active" ></slot></div> 
  <div :style="isActiveColor">
    <slot name="text"></slot>
  </div>
  
</div>
</template>

<script>
  export default {
    name: 'TabBarItem',
    props: {
      path: String,
      activeColor: {
        type: String,
        default: 'rgb(255, 41, 148)'
      }
    },
    computed: {
      isActive() {
        //判断传入的path是否被包含在当前patn中，从而动态决定iaActive的值
        return this.$route.path.indexOf(this.path)
      },
      isActiveColor() {
        return !this.isActive ? {color: this.activeColor} : {}
      }
    },
    methods: {
      itemClick() {
        this.$router.replace(this.path)
      }
    }, 
  }
</script>
<style lang="less">
/* @import url(); 引入css类 */
.tab-bar-item {
  flex: 1;
  text-align: center;
  font-size: 12px;
  img {
    width: 24px;
    height: 24px;
    margin-top: 5px;
    vertical-align: middle;
  }
}
</style>