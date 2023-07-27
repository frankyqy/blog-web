<template>
  <!--动态菜单-->
  <!--  根据登录状态 获取菜单列表-->
  <el-sub-menu>
    <template #title>
      <el-icon><Document /></el-icon>
      <span>{{title}}</span>
    </template>
    <el-menu-item-group v-for="(item,idx) in menuList" :title="item.tagName+'('+item.children.size+')'" :index="idx">
      <el-menu-item v-for="(child,cIdx) in item.children" :index="idx+'-'+cIdx" @click="open(child.path)">{{
          child.title
        }}
      </el-menu-item>
    </el-menu-item-group>
  </el-sub-menu>
</template>

<script>
import {Document} from "@element-plus/icons-vue";

export default {
  name: "DynamicMenu",
  components: {Document},
  data() {
    return {
      title: '文章列表',
      menuList: [{
        tagName: '公开文章',
        children: [{
          title: '从零开始的博客搭建(1',
          path: '@/assets/logs/从零开始的博客搭建(1.md'
        }, {
          title: '从零开始的博客搭建(2',
          path: '@/assets/logs/从零开始的博客搭建(2.md'
        }, {
          title: '从零开始的博客搭建(3',
          path: '@/assets/logs/从零开始的博客搭建(3.md'
        }
        ]
      }]
    }
  }
}
</script>

<style scoped>

</style>