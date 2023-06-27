<template>
  <div>
    <h1>{{ count }}</h1>
    <br><br>
    <button type="button" @click="count++">点击count+1</button>
  </div>
</template>

<script setup>

import {
  onActivated, onBeforeMount, onBeforeUnmount, onBeforeUpdate,
  onDeactivated, onErrorCaptured, onMounted, onUnmounted,
  onUpdated, ref
} from 'vue'

const count = ref(100)

onMounted(() =>
{
  console.log("onMounted")
})

onUpdated(() =>
{
  console.log("onUpdated")
})

onUnmounted(() =>
{
  console.log("onUnmounted")
})

onBeforeMount(() =>
{
  console.log("onBeforeMount")
})

onBeforeUpdate(() =>
{
  console.log("onBeforeUpdate")
})

onBeforeUnmount(() =>
{
  console.log("onBeforeUnmount")
})

onErrorCaptured(() =>
{
  console.log("onErrorCaptured")
})

onActivated(() =>
{
  console.log("onActivated")
})

onDeactivated(() =>
{
  console.log("onDeactivated")
})


</script>

<style scoped>

</style>
