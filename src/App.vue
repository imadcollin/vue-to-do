<template>
  <Todos m v-bind:todos="todos" v-on:del-todo="deleteTodo" />
  <AddItem v-on:add-Item="addItem" />
</template>

<script>
import Todos from "./components/Todos";
import AddItem from "./components/AddItem";
export default {
  name: "App",
  components: {
    Todos,
    AddItem,
  },
  data() {
    return {
      todos: [
        { id: 1, title: "title 1", status: true },
        { id: 2, title: "title 2", status: true },
        { id: 3, title: "title 3", status: false },
      ],
    };
  },
  methods: {
    deleteTodo(id) {
      this.todos = this.todos.filter((x) => x.id !== id);
    },
    addItem(newTodo) {
       this.todos = [...this.todos, newTodo];
    },
  },
};
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
