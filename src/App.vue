<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>
    {{title}}
  </h1>
  <input type="text" ref="name">
  <button @click="handleClick">Click me</button>
  <teleport to=".modals">
  <Modal v-show="showModal"  theme="sale" @close="handleClick">
    <h1>Yacine Says Hi!!!!</h1>
    <template v-slot:links>
      <a href="#">sing up here</a>
      <br>
      <a href="#">read more</a>
    </template>
  </Modal>
  </teleport>
  <button @click="toggleModal2">MOdal2</button>
    <teleport to=".modals">
  <Modal v-show="showModal2" >
    <h1>Hanane says hi</h1>
    <template v-slot:btn>
      <h2>Second Modal woohoo</h2>
      <button @click="closeModal2">Close Modal</button>
    </template>
  </Modal>
    </teleport>
</template>
<script>
import Modal from './components/Modal.vue'
export default {
  name: 'zApp',
  data(){
    return{
      title:"Khalitha vue :)",
      content:"whatever i want here",
      showModal:false,
      showModal2: false,

    }
  },
  methods:{
    handleClick(){
      console.log(this.$refs.name)
      this.$refs.name.focus()
      this.showModal=!this.showModal
    },
    closeModal2(){
      this.showModal2= false
    },
    toggleModal2(){
      this.showModal2=!this.showModal2
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
