<template>
  <div id="app">
    <MyTable :passGoods="goods">
      <template #header>
        <th>编号</th>
        <th>图片</th>
        <th>名称</th>
        <th>标签</th>
      </template>
      <template #body="{item, index}" >
        <td>{{ index + 1 }}</td>
        <td><img :src="item.picture" alt=""></td>
        <td>sb紫砂壶</td>
        <td>
          <MyTag :passGoods="item" v-model="item.tag"></MyTag>
        </td>
      </template>
    </MyTable>
  </div>
</template>

<script>
import MyTag from "./components/MyTag.vue"
import MyTable from ".//components/MyTable.vue"

export default {
  name: 'App',
  components: {
    MyTag,
    MyTable
},
  data() {
    return {
      goods: [
        {id: 101, picture: "https://th.wallhaven.cc/small/yx/yxqzpd.jpg", tag: "anime"},
        {id: 102, picture: "https://th.wallhaven.cc/small/qz/qzpkrr.jpg", tag: "nature"},
        {id: 103, picture: "https://th.wallhaven.cc/small/rr/rre161.jpg", tag: "wind"},
        {id: 104, picture: "https://th.wallhaven.cc/small/yx/yxkl1k.jpg", tag: "summer"},
        {id: 106, picture: "https://th.wallhaven.cc/small/85/858wmy.jpg", tag: "weather"},
      ]
    }
  },
  methods: {
  }
}
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  padding: 18px;

  display: flex;
  justify-content: center;
  flex-direction: column;

  border: 1px solid orangered;
  border-radius: 16px;
  box-shadow: 1px 1px 4px black;

}


</style>
