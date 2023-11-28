<template>
  <div id="app">
    <button @click="exit">退出按钮</button>
    <BaseA :isShow.sync="isShow"></BaseA>
  </div>
</template>

<script>
import BaseA from './components/BaseA.vue';


export default {
  name: 'App',
  components: {
    BaseA,
  },
  data() {
    return {
      isShow: true
    }
  },
  methods: {
    exit() {
      this.isShow = false
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

  display: flex;
  justify-content: center;
  flex-direction: column;

}


</style>
