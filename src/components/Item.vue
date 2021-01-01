<template>
    <div>
<h2>{{todo.title}}</h2>
    </div>
</template>

<script>
export default {
    name: "Item",
    props:["todo"]
        
}
</script>
<style scoped>
h2 {
    color: blueviolet;
    }
</style>
