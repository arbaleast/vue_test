<template>
  <div class="box" >
    <table>
      <thead>
        <tr>
          <slot name="header"></slot>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(item, index) in passGoods">
          <slot name="body" :item="item" :index="index"></slot>
        </tr>
      </tbody>
    </table>
  </div>
</template>
<script>

export default {
    name: "MyTable",
    props: {
      passGoods: Array
    },
    data() {
        return {};
    },
    methods: {
    },
    components: {  }
}
</script>
<style lang="less" scoped>
  th {
        width: 25%;
        padding: 15px;
        background-color: cadetblue;
      }
  tbody {
    tr {
      margin: 35px auto;
      td {
        margin-top: 15px;
      }

    }
  }
</style>
