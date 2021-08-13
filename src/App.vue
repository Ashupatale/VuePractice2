<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>Name  {{name}}</h1>
    <CompC/>

  <button @click="ShowPopup=true">Show Pop up</button>
    <PopUp v-show="ShowPopup" @close="ClosePopup"/>

    <Input />
  </div>

</template>

<script>
import CompC from './components/CompC.vue'
import PopUp from './components/Popup.vue'
import Input from './components/Input.vue'

export default {
  data(){
    return{
      name:"Welcome Aakash",
      ShowPopup:false,
    
    }

  },
  name: 'App',
  components: {
    CompC,
    PopUp,
    Input
  },
  methods:{
    ClosePopup(name){
      this.ShowPopup=false;
      console.log('name' , name)
    }
  },
  provide:{
    username:'Aakash Patale'
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
}
</style>
