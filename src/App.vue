<script setup>
import MyHeader from "@/components/container/MyHeader.vue";
import MySide from "@/components/container/MySide.vue";
import MyContent from "@/components/container/MyContent.vue";
import MyFooter from "@/components/container/MyFooter.vue";
</script>

<template>
  <el-container id="app" direction="vertical">
    <my-header/>
    <el-container>
      <my-side/>
      <el-container direction="vertical">
        <my-content/>
        <my-footer/>
      </el-container>
    </el-container>
  </el-container>
</template>

<style scoped>
#app {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 100%;
}
</style>
