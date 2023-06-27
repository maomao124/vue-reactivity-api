<template>

  <h1>{{ count }}</h1>
  <br><br>
  <button type="button" @click="plusOne">点击count+1</button>
  <br>
  <button type="button" @click="stop">点击取消监听</button>

</template>

<script setup>

import {ref, watchEffect} from 'vue'

const count = ref(100)

function plusOne()
{
  count.value++;
}

const stop = watchEffect(() =>
{
  console.log("count变化")
  console.log(count.value)
})


</script>

<style scoped>

</style>
