<template>
  <div class="box" v-show="isShow">
    <div class="header">
      <span>温馨提示</span>
      <button class="exit" @click="exit">X</button>
    </div>

    <div class="content">
      <p>你敢走___*( ￣皿￣)/#____</p>
    </div>

    <div class="footer">
      <button @click="exit">我不敢</button>
      <button @click="exit">咋的，不行啊</button>
    </div>
  </div>
</template>
<script>
 
export default {
  name: 'BaseA',
  props: {
    isShow: Boolean
  },
  data () {
    return {
    }
  },
  methods: {
    handler(e) {
      this.$emit("input", e.target.value)
    },
    exit() {
      console.log("triggled!!!");
      this.$emit("update:isShow", false)
    }
  }
}
</script>
<style lang="less" scoped>
.box {  
  width: 80%;
  height: 200px;
  margin: 20px auto;
  padding: 0 10px;

  border: 1px solid orangered;
  border-radius: 8px;

  display: flex;
  flex-direction: column;
  justify-content: space-around;

  .header {
    display: flex;
    text-align: center  ;
    justify-content: space-between;
    width: 100%;
    padding: 8px 0;
    

    border: 3px solid black;
    border-top: none;
    border-left: none;
    border-right: none;
  }
  .content {
    text-align: left;
    padding-left: 20px;
  }
  .footer {
    margin: 20px 8px;

    display: flex;
    justify-content: space-between;
  }
}
</style>
