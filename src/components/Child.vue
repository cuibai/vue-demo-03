<!--
 * @Author: cuibai 2367736060@qq.com
 * @Date: 2023-03-22 21:29:12
 * @LastEditors: cuibai 2367736060@qq.com
 * @LastEditTime: 2023-03-22 21:43:31
 * @FilePath: \vue3-demo-149\src\components\Child.vue
 * @Description: 
 * 
 * Copyright (c) 2023 by ${git_name_email}, All Rights Reserved. 
-->
<template>
  <div>
    child组件
    <p>{{ count }}</p>
    <button @click="validate">校验</button>
  </div>
</template>

<script setup>
import { ref, defineExpose } from 'vue'

const count = ref(0)
const validate = () => {
    console.log('校验表单')
}

</script>

<style>

</style>