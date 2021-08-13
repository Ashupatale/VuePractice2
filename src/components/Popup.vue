<template>
    <div>
        <h1>This is a PopUp</h1>
        <input type="text" v-model="name" />
        <br/>
        <button @click="$emit('close', name)">Close Pop-up</button>
    </div>
</template>

<script>
    export default {
       name:"Popup",
       emits:{
           close:(name)=>{
               if(!name){
                   return false
               } else {
                   return true
               }
           },
       }, 
       data(){
           return{
               name:'',
           }
       }

    }
</script>

<style scoped>

</style>