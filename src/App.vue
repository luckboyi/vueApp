<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div class="ceshi ">
      <div v-for="(item,index) in demo" :key="index">{{item}}</div>
    </div>
    <button @click="arrFn()">数组Push</button>
    <div v-for="(item,index) in obj" :key="index" v-if="!item.isShow">
      {{item.list}}{{item.name}}
    </div>
    <button @click="objFn">对象Push</button>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      msg: 'cdddd',
      data: 'ccc',
      demo: ['zz', 'bb'],
      obj: [
        {
          'list': 'xxx'
        }
      ]
    }
  },
  mounted() {
    this.obj[0].name = 123
    this.obj.push({ 'list': 'ceshi', isShow: false })
    this.demo.push('vvv')
  },
  methods: {
    arrFn() {
      this.demo.push('ccc')
    },
    objFn() {
      this.obj[0].isShow = true
      console.log(this.obj)
    }
  }
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
