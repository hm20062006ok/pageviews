<template>
  <div class="app-wrapper">
<!--    <sidebar class="sidebar-container"/>-->

<!--    <app-main/>-->
  </div>
</template>

<script>
import { Sidebar } from './components'
export default {
  name: 'Layout',
  components: {
    Sidebar
    // AppMain
  }
}
</script>

<style lang="scss" scoped>

.app-wrapper {
  position: relative;
  height: 100%;
  width: 100%;


  .sidebar-container {
    transition: width 0.28s;
    width: 57px !important;
    background-color: #304156;
    height: 100%;
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    z-index: 1001;
    overflow: hidden;
  }
}

</style>
