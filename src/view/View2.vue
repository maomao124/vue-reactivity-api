<template>

  <div>
    <h1>test1:{{ test1 }}</h1>
    <h1>test1.a:{{ test1.a }}</h1>
    <h1>test1.b:{{ test1.b }}</h1>

    <h1>test2:{{ test2 }}</h1>
    <h1>test2.a:{{ test2.a }}</h1>
    <h1>test2.b:{{ test2.b }}</h1>
  </div>

</template>

<script setup>

import {reactive, ref} from 'vue'

const test1 = ref({a: 1, b: 2})
console.log(test1.value)
test1.value.a++;
test1.value.b++;

const test2 = reactive({a: 5, b: 6})
console.log(test2)
test2.a++
test2.b++

</script>

<style scoped>

</style>
