<!--
 * @Author: cuibai 2367736060@qq.com
 * @Date: 2023-03-24 21:18:18
 * @LastEditors: cuibai 2367736060@qq.com
 * @LastEditTime: 2023-03-24 22:33:38
 * @FilePath: \vue3-demo-149\src\components\Sonn.vue
 * @Description: 
 * 
 * Copyright (c) 2023 by ${git_name_email}, All Rights Reserved. 
-->
<template>
    <div class="child-com" style="border: 10px solid #ccc; padding:5px" >
        chrld{{ count }}
        <button @click="changeCount(10)">change</button>
    </div>
</template>

<script setup>
import { inject } from "vue"
const count = inject('count')
const changeCount = inject('changeCount')
</script>

<style>

</style>