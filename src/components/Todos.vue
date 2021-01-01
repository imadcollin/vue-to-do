<template>
  <div class="Todos">
  <h1>{{msg}}</h1>
  <div v-bind:key="todo.id" v-for="todo in todos">
      
      <!-- <h3>Todos {{todo.id}} {{todo.title}}</h3> -->
      <Item v-bind:todo="todo"/>
  </div>
  </div>
</template>

<script>
import Item from './Item'; 
export default {
  name: 'Todos',
  components:{
      Item
      },
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
