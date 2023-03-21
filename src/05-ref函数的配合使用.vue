<template>
  <div>
    计数器{{count}}
    <button @click="count++">+1</button>
    <button @click="incremment()">-1</button>
  </div>
</template>

<script>
// 引入
import { ref } from 'vue'
export default {
    setup(){
        /**
         * 使用 ref 创造响应式数据
         * 再js中使用需要添加 .value 方法
         * 在模板中不需要
         */
        const count = ref(0)
        const incremment = () => {
            count.value -= 1
        }
        return{count,incremment}
    },
    

}
</script>

<style>

</style>