<template>
  <div class="box" v-show="isShow" v-loading="image">
    <div class="header">
      <span>温馨提示</span>
      <button class="exit" @click="exit">X</button>
    </div>

    <div class="content">
      <p>你敢走___*( ￣皿￣)/#____</p>
    </div>

    <div class="footer">
      <button @click="exit(false)"  >我不敢</button>
      <button @click="exit(true)"  >咋的，不行啊</button>
    </div>
    <img :src="image" alt="" width="100%" height="100%">
  </div>
</template>
<script>

export default {
  name: 'BaseA',
  props: {
    isShow: Boolean,
  },
  directives: {
    loading: {
      inserted(el, binding) {
        binding.value > 1 ? el.classList.remove("loading") : el.classList.add("loading")
      },
      update(el,binding) {
        binding.value.length > 1 ? el.classList.remove("loading") : el.classList.add("loading")
        console.log(binding, binding.value.length);
      }
    }
  },
  data () {
    return {
      image: ""
    }
  },
  methods: {
    handler(e) {
      this.$emit("input", e.target.value)
    },
    exit(value) {
      if (value) {
        alert("算你狠")
        this.$emit("update:isShow", false)
        
        return 
      } else {
        alert("不错不错，（￣︶￣）↗ ")
        this.$emit("update:isShow", false)
        return
      }

      this.$emit("update:isShow", false)

    }
  },
  created() {
    setTimeout(() => {
      this.image = "https://w.wallhaven.cc/full/2y/wallhaven-2y6wwg.jpg"
    }, 3000)
  }
}
</script>
<style lang="less" scoped>
.loading:before {
  width: 100%;
  height: 100%;
  background: url("https://gifdb.com/images/high/morning-coffee-loading-process-dg9uaxmp8giczrz2.webp") no-repeat center;
  content: "";

  position: absolute;
  left: 0;
  top: 0;
}
</style>
