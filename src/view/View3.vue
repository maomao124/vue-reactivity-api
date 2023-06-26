<template>

  <div>
    <h1>{{ count }}</h1>
    <h1>{{ obj.count }}</h1>
  </div>

</template>

<script setup>

import {reactive, ref} from 'vue'

const count = ref(1)
const obj = reactive({count})

// ref 会被解包
console.log(obj.count === count.value) // true

// 会更新 `obj.count`
count.value++
console.log(count.value) // 2
console.log(obj.count) // 2

// 也会更新 `count` ref
obj.count++
console.log(obj.count) // 3
console.log(count.value) // 3

</script>

<style scoped>

</style>
