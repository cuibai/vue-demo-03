<!--
 * @Author: cuibai 2367736060@qq.com
 * @Date: 2023-03-24 21:18:18
 * @LastEditors: cuibai 2367736060@qq.com
 * @LastEditTime: 2023-03-24 21:54:33
 * @FilePath: \vue3-demo-149\src\components\Sonn.vue
 * @Description: 
 * 
 * Copyright (c) 2023 by ${git_name_email}, All Rights Reserved. 
-->
<template>
  <div>
    sonn{{ money }}
    <button @click="fn">触发点击事件</button>
  </div>
</template>

<script setup>
/**
 * 利用vue3 的父子属性 
 * 获取数据
 * 最新的vue3 中 封装了很多编译器 有一些函数是不需要额外引入的
 */
// import {defineProps} from 'vue'

const props = defineProps({
    money: {
        type: Number,
        default: 0
    }
})
// vue3中没有this.$emit方法 使用自定义触发函数
const emit = defineEmits(['changeMoney']) // 自定义触发事件名称
const fn = () => {
    emit('changeMoney',props.money-20)
}
// 测试在js中直接输出参数
console.log(props.money)
</script>