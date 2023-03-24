<!--
 * @Author: cuibai 2367736060@qq.com
 * @Date: 2023-03-24 21:16:30
 * @LastEditors: cuibai 2367736060@qq.com
 * @LastEditTime: 2023-03-24 21:16:45
 * @FilePath: \vue3-demo-149\src\11-父子组件的调用.vue
 * @Description: 
 * 
 * Copyright (c) 2023 by ${git_name_email}, All Rights Reserved. 
-->
<template>
<Child ref="childref"></Child>
<button @click="fn">获取组件实例</button>
</template>

<script setup>
import Child from './components/Child.vue'
import {ref} from 'vue'
const childref = ref(null)
const fn = () => {
    console.log(childref.value)
}
</script>

<style>

</style>