<!--
 * @Author: cuibai 2367736060@qq.com
 * @Date: 2023-03-20 21:15:52
 * @LastEditors: cuibai 2367736060@qq.com
 * @LastEditTime: 2023-03-21 20:49:15
 * @FilePath: \vue3-demo-149\src\App.vue
 * @Description: 
 * 
 * Copyright (c) 2023 by ${git_name_email}, All Rights Reserved. 
-->
<template>
  <div class="app">123
    <button @click="state.age++">+1</button>
    <p>{{state.name}}</p>
    <p>{{state.age}}</p>
  </div>
</template>

<script>
import { reactive } from 'vue'
export default {
    setup(){
        // 把普通对象转换为 响应式数据
        const state = reactive({
            name:"jick",
            age:11
        })
        return{state}
    }
}
</script>

<style>

</style>