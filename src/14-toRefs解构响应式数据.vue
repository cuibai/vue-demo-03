<template>
  <div class="class">
    123
    <hr>
    {{ age }}
    {{ name }}
    <hr>
    {{ names }}
    {{ ages }}
  </div>
</template>

<script setup>
import { reactive ,toRefs } from 'vue'
const {name,age }  = reactive({
    name:'jack',
    age:22
})
/**从一个响应式数据中解构出来的数据就不具备响应式的特点了
 * 不在支持数据响应
 * 使用toRefs 处理响应式
 * 作用: 结构响应式数据 踩坑
 *  */ 
const user = reactive({
    names: 'meg',
    ages: 12,
    describes:"古神之躯"
})
// 解构
const {names,ages} = toRefs(user)



</script>

<style>

</style>