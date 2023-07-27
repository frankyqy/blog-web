<template>
  <!--账户组件 在header上显示为一个按钮-->
  <!--  未登录时 点击跳转到登录页面-->
  <!--  登录后 点击 展示账户卡片-->
  <el-avatar/>
</template>

<script>
import {User} from "@element-plus/icons-vue";

export default {
  name: "Account",
  computed: {
    User() {
      return User
    }
  }
}
</script>

<style scoped>

</style>