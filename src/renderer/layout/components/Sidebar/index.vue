<template>
  <div>
    <el-scrollbar wrap-class="scrollbar-wrapper">
      <el-menu
          :default-active="activeMenu"
          :collapse="isCollapse"
          :background-color="variables.menuBg"
          :text-color="variables.menuText"
          :unique-opened="false"
          :active-text-color="variables.menuActiveText"
          :collapse-transition="false"
          mode="vertical"
      >
        <sidebar-item v-for="route in routers" :key="route.path" :item="route" :base-path="route.path"/>
      </el-menu>
    </el-scrollbar>
  </div>
</template>

<script>
import SidebarItem from './SidebarItem'

export default {
  components: {SidebarItem},
  data () {
    return {
      routers: [
        {
          path: '/'
        }
      ]
    }
  },
  computed: {
    activeMenu () {
      return this.$route.path
    }
  }
}
</script>
