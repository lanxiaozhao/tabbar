<template>
  <div id="app">
    
    <main-tab-bar></main-tab-bar>
  </div>
</template>
<script>
  import MainTabBar from 'components/MainTabBar/MainTabBar'
  export default {
    name: 'App',
    components: {
      MainTabBar
    }
  }
</script>
<style lang="less">
  @import "assets/less/base.less"; 
</style>
