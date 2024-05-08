<template>
  <div class="wrapper">
    <h2 @click="test">Vue 项目 Demo</h2>
    <TabAndButton  title="测试卡片" />
  </div>
</template>

<script setup lang="ts">
import TabAndButton from './components/TabAndButton/index.vue'
import './app.css'
function test () {
  const flatRes = ['a', 'b', 'c', 'd', 5, [ 'e', 'f', 'g'], ['h', 'i']]
  const index =  flatRes.findIndex(i => i  === 'h')
  const i2 = flatRes.find(i => i ==='a')
  console.log('doubledNumbers squaredArray', flatRes, index, Object.values({ "DD": "1", "EE": "2"}))
  flatRes.fill(0, 2, 4);
}
</script>
<style scoped>
</style>