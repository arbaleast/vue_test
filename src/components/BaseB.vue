<template>
  <div >
    我是B组件(发布方)
    <button @click="pubMsg">发布通知</button>
  </div>
</template>
<script>
import Bus from '@/utils/EventBus';

export default {
  name: 'BaseB',
  data () {
    return {
    }
  },
  methods: {
    pubMsg() {
      Bus.$emit("sendMsg", "我是一条消息")
    }
  }
}
</script>
<style lang="less" scoped>

</style>
