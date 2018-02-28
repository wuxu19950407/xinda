<template>
  <div>
    <h2 v-bind:class="style">欢迎来到{{reverseInfo}}---{{info}}</h2>
    <router-view></router-view>
    <p v-if="b">这是文字</p>
    <p v-show="c">这是文字能隐藏的</p>
    <p>这是文字{{fullName}}</p>
    <button v-on:click="foo">按钮</button>
    <p>我被电击了{{count}}次</p>
    <input type="text" v-model="info">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      info: '德莱联盟',
      style: 'text',
      b : true,
      c : 1,
      fristName: '旭',
      lastName: '吴',
      count : '0'
    }
  },
  methods:{
    foo:function(event){
      // this.style = 'ppp'
      this.fullName = '孙 悟空';
      this.c = false;
      console.log(event.target);
    }
  },
  computed:{
    reverseInfo(){
      return this.info.split('').reverse().join('');.0
    },
    fullName:{
      get(){
        return this.fristName+' '+this.lastName;
      },
      set(newValue){
        var names = newValue.split(' ');
        this.fristName = names[0];
        this.lastName = names[names.length-1]
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">

  .text{
    color: red;
  }
  .ppp{
    color: green;
  }
</style>