<template>
  <div class="box" >
    我是A组件
  </div>
</template>
<script>

export default {
  name: 'BaseA',
  provide() {
    return {
      num: this.num,
      list: this.list
    }
  },
  data () {
    return {
      num: 20,
      list: {
        name: "annie",
        age: 17
      }
    }
  }
}
</script>
<style lang="less" scoped>
.box {  
  width: 100px;
  height: 100px;
  margin: 20px 50%;
  
  border: 1px solid orangered;
  border-radius: 8px;

  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
