<template>
  <div id="app" class="d-flex flex-column">
    <div class="nav">
      <div
        class="nav-left col-2 d-flex justify-content-center align-items-center mr-auto"
      >
        ZPS
      </div>
      <div
        class="nav-right d-flex justify-content-end align-items-center m-right-10"
      >
        <i class="el-icon-user-solid"></i>
      </div>
    </div>
    <div class="main d-flex flex-row flex-grow-1">
      <div class="aside col-2"></div>
      <div class="content flex-fill">
        <div v-html="compiledFunction('testName')"></div>
      </div>
    </div>
  </div>
</template>

<script>
const pug = require('pug')
const fs = require('fs')
// 编译这份代码
const compiledFunction = pug.compileFile('@/views/pugComponent/test.pug')
export default {
  data() {
    return {
      testData: ''
    }
  },
  mounted() {
    console.log(fs)
  },
  methods: { compiledFunction }
}
</script>
>

<style lang="less">
html,
body {
  width: 100%;
  height: 100%;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: inherit;
}
</style>

<style lang="less" scoped>
.nav {
  background: #2c3e50;
  height: 60px;
  color: #ffffff;
  > .nav-left {
    border-right: 1px solid #cccccc;
  }
}

.main {
  background: #cccccc;
  > .aside {
    background: #ffffff;
  }
}
</style>
