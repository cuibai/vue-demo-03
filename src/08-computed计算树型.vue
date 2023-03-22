<template>
  <div>
    <p>分数:{{ scoreList }}</p>
    <p>优秀:{{ betterList }}</p>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
const scoreList = ref([80, 100, 90, 70, 60])
// 计算属性
const betterList = computed(() => scoreList.value.filter((item) => item > 90))
// 改变数据结构 计算树型
setTimeout(() => {
    scoreList.value.push(92,66)
},300)
</script>

<style>

</style>