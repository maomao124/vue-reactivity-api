<template>
  <div>
    <h2>count: {{ readonly1.count }}</h2>
    <h2>a.a1: {{ readonly1.a.a1 }}</h2>
    <h2>a.a2: {{ readonly1.a.a2 }}</h2>

  </div>
</template>

<script setup>
import {readonly} from 'vue'

const readonly1 = readonly({count: 1, a: {a1: 1000, a2: 30243}})

console.log(readonly1.count)
console.log(readonly1.a.a1)
console.log(readonly1.a.a2)
try
{
  readonly1.count++;
}
catch (e)
{
  console.log(e)
}
try
{
  readonly1.a.a1++;
}
catch (e)
{
  console.log(e)
}
try
{
  readonly1.a.a2++;
}
catch (e)
{
  console.log(e)
}

</script>

<style scoped>

</style>
