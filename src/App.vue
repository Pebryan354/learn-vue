<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <input type="text" ref="name"> -->
  <button @click=handleClick>Tekan</button>
  <!-- <HelloWorld msg="Welcome to my Vue.js App" name="Pebryan" url="https://my-appweb.com" /> -->
  <h1>{{ title }}</h1>

  <Modal :modal="clsModal" :backdrop="clsBckdrp" />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Modal from "./components/Modal.vue";

export default {
  name: 'App',
  components: {
    Modal
  },
  data() {
    return {
      title: 'My first vue app.',
      clsModal : '',
      clsBckdrp : ''
    }
  },
  methods: {
    handleClick() {
      this.clsModal = 'modal'
      this.clsBckdrp = 'backdrop'
      // console.log(this.$refs.name)
      // this.$refs.name.classList.add('active')
      // this.$refs.name.focus()
    }
  },
  // components: {
  //   HelloWorld
  // }
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
}

h1 {
  border-bottom: 1px solid #ddd;
  padding-bottom: 10px;
}
</style>
