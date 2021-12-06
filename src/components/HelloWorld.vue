<script setup lang="ts">
import { ref,createApp } from 'vue'
import { Button } from '@nutui/nutui';
const app = createApp();
app.use(Button);

defineProps<{ msg: string }>()
const count = ref(0)

</script>

<template>
  <h1>{{ msg }}</h1>
  <button type="button" @click="count++">count is: {{ count }}</button>
  <Button type="primary">主要按钮</Button>
  <Button type="info">信息按钮</Button>
  <Button type="default">默认按钮</Button>
  <Button type="danger">危险按钮</Button>
  <Button type="warning">警告按钮</Button>
  <Button type="success">成功按钮</Button>
</template>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
