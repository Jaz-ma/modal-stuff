<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>I learn frameworks while using VIM because i hate myself</h1>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'zApp',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  height: 81vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>
