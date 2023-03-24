<template>
  <div
   class="app-page"
   style="border: 10px solid #ccc; padding:5px" 
  >
    app组件
    <Parent></Parent>
  </div>
</template>

<script setup>
import { ref,provide } from 'vue'
import Parent from './components/Parent.vue'

/**
 * provides和inject
 * 跨组件通讯
 * provides: 提供依赖的数据和函数
 * inject: 获取provide所提供的数据
 */
//数据的相互传递
// 数据的修改原则 谁定义谁修改
const count = ref(0)
// 其它级别想修改数据 需要通过函数去操作
const changeCount = (val) => { 
    count.value += val
}
// provide('数据名称','具体数据')
provide('count', count)
provide('changeCount', changeCount)

</script>

<style>

</style>