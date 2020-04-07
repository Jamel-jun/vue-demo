<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <!-- <HelloWorld/> -->
    <!-- <Demo01/> -->
    <!-- <Demo02/> -->
    <!-- <Demo03/> -->
    <Demo04/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Demo01 from './components/Demo01'
import Demo02 from './components/Demo02'
import Demo03 from './components/列表渲染'
import Demo04 from './components/模糊查询'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Demo01,
    Demo02,
    Demo03,
    Demo04
  }
}
</script>

<!--<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>-->
