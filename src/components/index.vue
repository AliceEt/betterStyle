<script setup lang="ts">
import { ref } from 'vue'
import { Avatar, Button, Icon, Rate, BackTop, Row, Col } from '@nutui/nutui'
// eslint-disable-next-line no-debugger
debugger
// import '@nutui/nutui/dist/style.css'
// const app = createApp({})
// app.use(Avatar)
// app.use(Button)
// app.use(Icon)
// app.use(Rate)
// app.use(BackTop)
// app.use(Layout)
// app.use(Row)
// app.use(Col)

defineProps<{ msg: string }>()
const count = ref(0)
const value = ref(3)
const onChange = (val: any) => {
  console.log(val)
}
const handleClick = () => {
  console.log('触发返回顶部')
}
</script>

<template>
  <h1>{{ msg }}</h1>
  <button type="button" @click="count++">count is: {{ count }}</button>
  <Button type="primary">主要按钮</Button>
  <Button type="info">信息按钮</Button>
  <Button type="default">默认按钮</Button>
  <Rate v-model="value" @change="onChange"></Rate>
  <Avatar
    size="normal"
    icon="https://img12.360buyimg.com/imagetools/jfs/t1/143702/31/16654/116794/5fc6f541Edebf8a57/4138097748889987.png"
  ></Avatar>
  <Icon
    size="100"
    name="https://img11.360buyimg.com/imagetools/jfs/t1/137646/13/7132/1648/5f4c748bE43da8ddd/a3f06d51dcae7b60.png"
  ></Icon>
  <div>
    <Row :gutter="10">
      <Col :span="8">
        <div class="flex-content">span:8</div>
      </Col>
      <Col :span="8">
        <div class="flex-content flex-content-light">span:8</div>
      </Col>
      <Col :span="8">
        <div class="flex-content">span:8</div>
      </Col>
    </Row>
  </div>

  <BackTop @click="handleClick" el-id="elId" :distance="100" :bottom="90"></BackTop>
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
