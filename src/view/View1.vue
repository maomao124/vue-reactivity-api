<template>
  <div>
    <h1>a:{{ a }}</h1>
    <h1>b:{{ b }}</h1>
  </div>
</template>

<script setup>

import {ref} from 'vue'

const a = ref(120);
console.log(a.value)
const b = ref("hello");
console.log(b)
console.log(b.value)

</script>

<style scoped>

</style>
