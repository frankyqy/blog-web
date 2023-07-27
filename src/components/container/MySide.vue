<template>
  <el-aside class="menu" width=null>
    <el-scrollbar>
      <el-menu
          default-active="1"
          :collapse="isCollapse">
        <el-menu-item index="1">
          <template #title>
            <span>首页</span>
          </template>
          <el-icon>
            <home-filled/>
          </el-icon>
        </el-menu-item>
        <el-menu-item index="2">
          <template #title>
            <el-input/>
          </template>
          <el-icon>
            <Search/>
          </el-icon>
        </el-menu-item>
        <dynamic-menu/>
      </el-menu>
    </el-scrollbar>
    <el-menu>
      <el-menu-item index="99" @click="isCollapse=!isCollapse" style="bottom: 0">
        <el-icon>
          <Fold v-if="isCollapse"/>
          <Expand v-else/>
        </el-icon>
      </el-menu-item>
    </el-menu>

  </el-aside>
</template>

<script>
import {Expand, Fold, HomeFilled, House, Location, Search} from "@element-plus/icons-vue";
import DynamicMenu from "@/components/DynamicMenu.vue";

export default {
  name: "MySide",
  components: {DynamicMenu, Search, HomeFilled, House, Location, Fold, Expand},
  data() {
    return {
      isCollapse: false
    }
  }
}
</script>

<style scoped>
.menu {

}

.flex-grow {
  flex-grow: 1;
}
</style>