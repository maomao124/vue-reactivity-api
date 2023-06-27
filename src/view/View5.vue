<template>
  <div>
    <h2>{{ plus }}</h2>
    <h2>{{ plus2 }}</h2>
  </div>
</template>

<script setup>

import {computed, ref} from 'vue'

const count1 = ref(100)
const count2 = ref(300)
console.log(count1.value)
console.log(count2.value)
const plus = computed(() =>
{
  return count1.value + count2.value;
})

console.log(plus.value)

try
{
  plus.value++;
}
catch (e)
{
  console.log(e)
}

const count3 = ref(200)
const count4 = ref(600)
const plus2 = computed({
  get: () =>
  {
    return count3.value + count4.value;
  },
  set: (v) =>
  {
    count3.value = v;
    count4.value = v;
  }
})
console.log(plus2.value)
plus2.value++
console.log(plus2.value)


</script>

<style scoped>

</style>
