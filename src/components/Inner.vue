<template>
  <div>
    <h2>这是登陆注册公共头部</h2>
    <router-view></router-view>
    <h2>这是登陆注册公共脚部</h2>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">

</style>