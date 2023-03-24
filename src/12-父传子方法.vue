<!--
 * @Author: cuibai 2367736060@qq.com
 * @Date: 2023-03-20 21:15:52
 * @LastEditors: cuibai 2367736060@qq.com
 * @LastEditTime: 2023-03-24 21:59:56
 * @FilePath: \vue3-demo-149\src\App.vue
 * @Description: 
 * 
 * Copyright (c) 2023 by ${git_name_email}, All Rights Reserved. 
-->
<template>
    <Sonn :money="money" @change-money="fn"></Sonn>
  <div>
123
  </div>
</template>

<script setup>
import  Sonn from "./components/Sonn.vue"
import { ref } from "vue"
</script>
const money = ref(100)
const fn = (val) => {
    consolse.log('change-money',val)
}
<style>

</style>