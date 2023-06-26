<template>

  <div>
    <h1>{{ books[1].value }}</h1>
    <h1>{{ map.get('count').value }}</h1>
    <h1>{{ obj.count }}</h1>
    <h1>{{ count }}</h1>
  </div>

</template>

<script setup>

import {reactive, ref} from 'vue'

//当访问到某个响应式数组或 Map 这样的原生集合类型中的 ref 元素时，不会执行 ref 的解包
const books = reactive([ref('1'), ref('2'), ref('3')])
// 这里需要 .value
console.log(books[0].value)

const map = reactive(new Map([['count', ref(100)]]))
// 这里需要 .value
console.log(map.get('count').value)


//将一个 ref 赋值给一个 reactive 属性时，该 ref 会被自动解包
const count = ref(1000)
const obj = reactive({})

obj.count = count

console.log(obj.count) // 1000
console.log(obj.count === count.value) // true
console.log(count)
console.log(obj.count)

</script>

<style scoped>

</style>
