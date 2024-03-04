<script setup lang="ts">
import { onMounted } from 'vue'
import { reqLogin } from './api/user'

onMounted(() => {
  reqLogin({ username: 'admin', password: '123456' })
})
</script>

<template>
  <div>
    <h1 class="text-title">Vue starter 小專案模板</h1>
    <p class="text-green-500 font-bold">Tailwind 已套用版本</p>
    <router-view></router-view>
    <el-button type="primary">elementPlus 引入 & 調整自訂樣式</el-button>
  </div>
</template>

<style lang="scss" scoped>
.text-title {
  font-size: 3rem;
  font-weight: bold;
  color: $color;
}
</style>
