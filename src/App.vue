<template>
  <div id="app">
    <div id="nav">
      <MainTabBar/>
      <RouterView/>
    </div>
  </div>
</template>


<script>
  import MainTabBar from "./components/content/mainTabbar/MainTabBar";
export default {
  name:"app",
  components:{
    MainTabBar,

  }
}




</script>




<style lang="stylus">
@import "assets/css/base.css"
</style>
