<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>
    {{title}}
  </h1>
  <input type="text" ref="name">
  <button @click="handleClick">Click me</button>
  <Modal/>
</template>

<script>
import Modal from './components/Modal.vue'
export default {
  name: 'zApp',
  data(){
    return{
      title:"fuck me sideways"
    }
  },
  methods:{
    handleClick(){
      console.log(this.$refs.name)
      this.$refs.name.focus()
    }
  },
  components:{
    Modal,
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
