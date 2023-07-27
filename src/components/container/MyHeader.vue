<template>
  <el-header class="header">
    <el-page-header title='技术分享日志' :icon="null">
      <template #content>
        <el-text size="small">Life is like a boat.</el-text>
      </template>
      <template #extra>
        <account/>
      </template>
    </el-page-header>
  </el-header>
</template>
<script>

import Account from "@/components/Account.vue";

export default {
  name: "MyHeader",
  components: {Account}
}
</script>

<style scoped>
.header {
  position: relative;
  width: 100%;
  background-color: #66ccff;
  padding-top: 5px;
}
</style>