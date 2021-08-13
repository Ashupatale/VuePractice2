<template>
<div>
  <h1>Component E  </h1>
  <h3>name of User  {{username}}</h3>
</div>
</template>

<script>

export default {
    name:"CompE",
    inject:['username'],

}
</script>

<style>

</style>