<template>
    <div class="item" v-bind:class='{"status":todo.status}'>
<h2> {{todo.title}} -  status
<input type="checkbox" v-model="changeStatus">   <button class="del" @click="$emit('del-todo',todo.id)"> delete</button>

</h2>
 
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
.del {
    float:right;
    margin-right: 10%;
}
</style>
