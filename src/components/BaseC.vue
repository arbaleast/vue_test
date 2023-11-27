<template>
  <div >
    <span>{{ num }}</span>
    <br>
    <span>{{ list.name }}</span>
    <span>{{ list.age }}</span>
  </div>
</template>
<script>
export default {
  name: 'BaseC',
  inject:['num','list'],
  data () {
    return {
    }
  },
}
</script>
<style lang="less" scoped>

</style>
