<template>
  <div class="box" >
    我是B组件(发布方)
    <br>
    <BaseC></BaseC>
  </div>
</template>
<script>
import Bus from '@/utils/EventBus';
import BaseC from './BaseC.vue';

export default {
    name: "BaseB",
    data() {
        return {};
    },
    methods: {
        pubMsg() {
            Bus.$emit("sendMsg", "我是一条消息");
        }
    },
    components: { BaseC }
}
</script>
<style lang="less" scoped>
.box {
  width: 100px;
  height: 100px;
  margin: auto 50%;

  border: 1px solid orangered;
  border-radius: 8px;

  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
