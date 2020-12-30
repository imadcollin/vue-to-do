<template>
  <Todos m v-bind:todos="todos"/>
</template>

<script>
import Todos from './components/Todos'
export default {
  name: 'App',
  components: {
    Todos
  },
   data(){
     return {
       todos:[
         {id:1,
         title: "title 1",
         status: true
         },
           {id:2,
         title: "title 2",
         status: true
         },
           {id:3,
         title: "title 3",
         status: false
         }
     ]
     }
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
}
</style>
