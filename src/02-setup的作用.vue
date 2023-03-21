<!--
 * @Author: cuibai 2367736060@qq.com
 * @Date: 2023-03-20 21:15:52
 * @LastEditors: cuibai 2367736060@qq.com
 * @LastEditTime: 2023-03-21 20:41:51
 * @FilePath: \vue3-demo-149\src\setup的作用.vue
 * @Description: 
 * 
 * Copyright (c) 2023 by ${git_name_email}, All Rights Reserved. 
-->
<!--
 * @Author: cuibai 2367736060@qq.com
 * @Date: 2023-03-20 21:15:52
 * @LastEditors: cuibai 2367736060@qq.com
 * @LastEditTime: 2023-03-20 21:41:09
 * @FilePath: \vue3-demo-149\src\App.vue
 * @Description: 
 * 
 * Copyright (c) 2023 by ${git_name_email}, All Rights Reserved. 
-->
<template>
<div>
    {{msg}}
    <button @click="say">say</button>
</div>
</template>

<script>
/**
 * setup 
 * 1. 是组合式API的肉蔻
 * 2. 比 beforCreate执行更早
 * 3. 没有 this 实例 
 */
export default{
    setup(){
        // console.log("setup")
        // 数据给模板
        let msg = 'vue3'
        const say = () =>{
            msg = 'vue2'
            console.log(msg)
        }
        return{msg,say}
    }, 
    beforCreate(){
        console.log("beforCreate")
    }
}

</script>



<style scoped>

</style>
