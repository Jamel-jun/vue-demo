<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <!-- <HelloWorld/> -->
    <!-- <Demo01/> -->
    <Demo02/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Demo01 from './components/Demo01'
import Demo02 from './components/Demo02'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Demo01,
    Demo02
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
