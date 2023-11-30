<template>
  <div class="box" >
    <div class="my-tag">
      <input v-focus
        v-if="isEdit"
        @blur="isEdit = false "
        type="text"
        @keyup.enter="handlerTag"
        >
      <div 
        v-else
        @dblclick="isEdit = true"
        >{{ passGoods.tag }}</div>
    </div>
  </div>
</template>
<script>

export default {
  name: 'MyTag',
  props: {
    passGoods: Object
  },
  directives: {
    focus: {
      inserted(el) {
        el.focus()
      },
    }
  },
  data () {
    return {
      isEdit: false
    }
  },
  methods: {
    handlerTag(e) {
      console.log(e.target.value);
      this.$emit("input", e.target.value)
    },
  },
  created() {
  }
}
</script>
<style lang="less" scoped>

</style>
