<template>

  <h1>{{ count }}</h1>
  <br><br>
  <button type="button" @click="plusOne">点击count+1</button>
  <br>
  <button type="button" @click="stop">点击取消监听</button>



</template>

<script setup>

import {ref, watch} from 'vue'

const count = ref(100)

function plusOne()
{
  count.value++;
}

const stop = watch(count, (newValue, oldValue) =>
{
  console.log("监听到count变化", newValue, oldValue)
})


</script>

<style scoped>

</style>
