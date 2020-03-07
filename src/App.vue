<template>
  <div id="app">
    <div id="tab-bar">
      <div class="tab-bar-item">首页</div>
      <div class="tab-bar-item">首页</div>
      <div class="tab-bar-item">首页</div>
      <div class="tab-bar-item">首页</div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'App',
  components: {
    
  }
}
</script>
<style lang="less">
  @import "./assets/less/base.less";
  #tab-bar {
    display: flex;
    height: 49px;
    background-color: #f6f6f6;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    box-shadow: 0 -1px 1px rgba(136, 136, 136, 0.2);
    .tab-bar-item {
      flex: 1;
      text-align: center;
    }
  }
</style>
