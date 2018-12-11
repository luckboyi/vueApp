<template>
  <div id="app">
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

<style lang="scss" scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: $mainCol;
  @include fz(16px);
  margin-top: torem(120px);
}
</style>
