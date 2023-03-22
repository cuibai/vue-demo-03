<template>
  <div>
    <h1 ref="href">123</h1>
    <button @click="fn">change</button>
  </div>
</template>

<script setup>
import {ref, onMounted} from 'vue'

const href = ref(null)
onMounted(() => {
    console.log(href.value.innerText)
})
const fn = () => {
    href.value.innerText = '4556'
}
</script>

<style>

</style>