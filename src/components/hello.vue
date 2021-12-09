<script setup lang="ts">
import { ref, createApp } from 'vue'
import { Button, Icon } from '@nutui/nutui'
import { randomString, uniqueArray } from 'js-lib-vue'
const app = createApp({})
app.use(Button)
app.use(Icon)

defineProps<{ msg: string }>()
const count = ref(0)
console.log('randomString==', randomString(16))
console.log('uniqueArray==', uniqueArray([1, 2, 3, 2, 3, 5, 9, 8, 5]))
// console.log('countOccurrences===', countOccurrences([1, 3, 3, 4, 5, 3, 6, 7], 3))
// console.log('add==', add(16, 3))
// console.log('substract==', substract(16, 3))

// const arr = [
//   { id: '1001', weight: 50 },
//   { id: '1002', weight: 80 },
//   { id: '1003', weight: 120 },
//   { id: '1004', weight: 40 }
// ]
// console.log('weight==', fn(arr, 'weight'))
</script>

<template>
  <h1>{{ msg }}</h1>
  <div class="btn">
    <Button type="success" @click="count++">count is: {{ count }}</Button>
  </div>
  <Button type="primary">主要按钮</Button>
  <Button type="info">信息按钮</Button>
  <Button type="default">默认按钮</Button>
  <div class="btn">
    <Icon
      size="100"
      name="https://img11.360buyimg.com/imagetools/jfs/t1/137646/13/7132/1648/5f4c748bE43da8ddd/a3f06d51dcae7b60.png"
    ></Icon>
  </div>
</template>

<style scoped>
.btn {
  margin: 10px;
}
</style>
