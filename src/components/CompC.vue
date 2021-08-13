<template>
<div>
  <h1>Component C</h1>
  <CompD/>
</div>
</template>

<script>
import CompD from './CompD.vue'

export default {
    name:"CompC",

    components:{
        CompD,
    }

}
</script>

<style>

</style>