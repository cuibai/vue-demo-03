<template>
  <div>
    001
  </div>
</template>

<script>
import reactive的使用Vue from './reactive的使用.vue'
export default {
    setup() {
        /**
         * 是对象知道字段
         * 
         */
        const form = reactive({
            username: '12',
            password:'1234',
        })
        // 后台返回的数据对象
        const data = ref(null)
        const res = await axios.get('/user')
        // 给 data  赋值
        data.value = res
        return {}
    }
}
</script>

<style>

</style>