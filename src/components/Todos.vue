<template>
  <div class="Todos">
  <h1>{{msg}}</h1>
  <div v-bind:key="a.id" v-for="a in todos">
      
      <h3>Todos {{a.id}} {{a.title}}</h3>
  </div>
  </div>
</template>

<script>
export default {
  name: 'Todos',
  props: {
    msg: String,
    todos: Array 
  }
// props:["todos"]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color:#000;
}
</style>
