<template>
  <div>
    {{ count }}
    <button @click="count++">++</button>
    <p>姓名: {{ user.name }}</p>
    <p>性别: {{ user.info.gender }}</p>
    <p>年龄: {{ user.info.age }}</p>
    <button @click="$event=>user.name='tom'">修改</button>
    <button @click="$event=>user.info.age++">改年龄</button>
  </div>
</template>

<script setup>
/**watch 的用法
 * 1. 一个数据
 * 2. 多个数据
 * 3. 监听一个对象
 * 4. 监听多个对象 
 * 5. 默认执行 
 */
import { ref, watch, reactive} from 'vue'
//1
const count = ref(0)
watch(count, (nval, oval) => {
    console.log(nval, oval)
    
})
const user = reactive({
    name: 'user',
    info: {
        gender: 'man',
        age: '10'
    }
})
//2.
watch([count, user], () => {
    console.log('数据发生改变')
})
//3.
watch(() => user.name, () => {
    console.log('name change')
})
//4. 
watch(() => user.info, () => {
    console.log('处理复杂数据的监听')
}, {
    // 开启深度监听
    deep:true
})
// 5. 
watch(count, () => {
    console.log('默认执行监听')
}, {
    immediate:true
})


</script>

<style>

</style>