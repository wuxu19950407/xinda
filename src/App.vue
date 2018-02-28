<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <h1>公共头部</h1>
    <router-link to="/outter/register">注册</router-link>
    <router-view/>
    <h1>公共尾部</h1>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
