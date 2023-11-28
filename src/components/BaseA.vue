<template>
  <div class="box" @change="handler">
    <select :value="cityId">
      <option value="100">上海</option>
      <option value="101">北京</option>
      <option value="102">杭州</option>
      <option value="103">深圳</option>
      <option value="104">广州</option>
    </select>
  </div>
</template>
<script>
 
export default {
  name: 'BaseA',
  props: {
    cityId: String
  },
  data () {
    return {
      num: 20,
      list: {
        name: "annie",
        age: 17
      }
    }
  },
  methods: {
    handler(e) {
      this.$emit("passId", e.target.value)
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
