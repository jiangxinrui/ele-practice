<template>
  <div id="app">
    
    <router-view></router-view>

    <navs></navs>

  </div>
</template>

<script>
//引入底部导航栏
import Navs from './common/Navs.vue';

export default {
  components: {
    [Navs.name]: Navs
  }
}
</script>

<style>
html, body, #app{
    width: 100%;
    height: 100%;
    touch-action: none; /*解决iscroll拖动卡顿的问题*/
}

</style>
