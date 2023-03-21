<template>
  <div class="div1">
    <button @click="toggle">显示隐藏</button>
    <img v-show="show" src="./img/001.png" alt="B">

    计数器:{{ count }} <button @click="increment">加</button>
  </div> 

</template>

<script setup>
const say = () => console.log('say sommthing')
//
import { ref } from 'vue'
const show = ref(true)
const toggle = () => {
    show.value = !show.value
}
// ++
const count = ref(0)
const increment = () => {
    count.value++
}
</script>

<style>

</style>