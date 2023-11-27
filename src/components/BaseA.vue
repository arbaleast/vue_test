<template>
  <div class="box" >
    <span>我是A组件(接收方)
      <br>
      {{ msg }}
    </span>
  </div>
</template>
<script>
import Bus from "../utils/EventBus"

export default {
  name: 'BaseA',
  data () {
    return {
      msg: ""
    }
  },
  created() {

    Bus.$on("sendMsg", (msg) => {
      this.msg = msg
    })
  }
}
</script>
<style lang="less" scoped>
.box {  
  border-width: 1.5px;
  border-radius: 8px;
  border-color: orangered;

  span {
    display: flex;
    justify-content: center;
    width: 80%;
    height: 200px;



    align-items: center;
  }

}
</style>
