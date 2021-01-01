<template>
    <div class="item" v-bind:class='{"status":todo.status}'>
<h2>{{todo.id}}  {{todo.title}}
<input type="checkbox" v-model="changeStatus">
<label for="checkbox">{{changeStatus}}</label>

</h2>
  <input v-model="message" placeholder="edit me" />
  <p>Message is: {{ message }}</p>
  <button @click="$emit('del-todo',todo.id)"> delete</button>
</div>

</template>

<script>
export default {
    name: "Item",
    props:["todo"],
    data(){
        return { changeStatus:  this.todo.status,
        message: " "}
        },
    methods:{
      
            },
        
}
</script>
<style scoped>
.item {
    background-color: bisque;
    border: outset;

    }
h2 {
    color: blueviolet;
    }
.status{
    background-color: cadetblue;
    }    
</style>
