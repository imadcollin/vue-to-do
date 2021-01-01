<template>
  <div>
    <h1>Add Item</h1>
    <form @submit.prevent="addItem(e)">
      <input type="text" v-model="title" placeholder="Add an item" />
      <button type="submit" value="submit">Add</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "AddItem",
  data() {
    return { title: "" };
  },
  methods: {
    addItem() {
      const newtodo = {
        id: Math.floor(Math.random()*10),
        title: this.title,
        status: false,
      };
      this.$emit("add-Item", newtodo);
      this.title="";
    },
  },
};
</script>

<style scoped></style>
