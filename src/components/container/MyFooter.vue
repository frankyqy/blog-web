<template>
  <el-footer class="footer">
    <el-row justify="end">
      <el-col>
        <el-text>
          frankyqy@hotmail.com
        </el-text>
      </el-col>
    </el-row>
    <el-row justify="end">
      <el-col>
        <el-link href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=43010402001258">
          <el-image :src="logo"/>
          湘公网安备 43010402001258号
        </el-link>
      </el-col>
    </el-row>
    <el-row justify="end">
      <el-col>
        <el-link href="https://beian.miit.gov.cn/">湘ICP备2022007764号-1</el-link>
      </el-col>
    </el-row>

  </el-footer>
</template>

<script setup>
import logo from '@/assets/img/beian.png'
</script>

<style scoped>
.footer {
  text-align: right;
  height: 80px;
  background: var(--el-color-info-dark-2);
}
</style>