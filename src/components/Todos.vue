<template>
  <div class="Todos">
    <h1>{{ msg }}</h1>
    <div v-bind:key="todo.id" v-for="todo in todos" todo_prop_sync="todo">
      <Item v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)" />
    </div>
  </div>
</template>

<script>
import Item from "./Item";
export default {
  name: "Todos",
  components: {
    Item,
  },
  props: {
    msg: String,
    todos: Array,
  },
};
</script>

<style scoped>
h1 {
  color: #000;
}
</style>
