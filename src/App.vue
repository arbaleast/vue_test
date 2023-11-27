<template>
  <div id="app">
    <BaseA></BaseA>
    <BaseB></BaseB>
  </div>
</template>

<script>
import BaseA from './components/BaseA.vue';
import BaseB from './components/BaseB.vue';


export default {
  name: 'App',
  components: {
    BaseA,
    BaseB
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
