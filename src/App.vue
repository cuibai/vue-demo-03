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