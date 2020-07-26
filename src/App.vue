<template>
  <div id="app">
    <nav></nav>
    <b-container>
      <img alt="Vue logo" src="./assets/logo.png">
      <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
      <props msg="Application With Vue-Bootstrap"/>
    </b-container>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import props from './components/props.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    props
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  font-size: 20px;
  color: #2c3e50;
}
#app img {
  margin-top: 40px;
}
nav {
  width: 100%;
  height: 60px;
  background-color: #2c3e50;
}
</style>
