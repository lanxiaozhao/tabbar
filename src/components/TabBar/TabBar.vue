<!-- TabBar -->
<template>
<div id="tab-bar">
  <slot></slot>
</div>
</template>

<script>
  export default {
  name: 'TabBar'
  }
</script>
<style lang="less">
/* @import url(); 引入css类 */
  #tab-bar {
    display: flex;
    height: 49px;
    background-color: #f6f6f6;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    box-shadow: 0 -1px 1px rgba(136, 136, 136, 0.2);
  }
</style>