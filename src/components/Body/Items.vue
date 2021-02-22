<template>
  <div>
    <div
      v-bind:key="todoItem.id"
      v-for="todoItem in todosList"
      class="list-group"
    >
      <Item v-bind:item="todoItem" v-on:delTodo="$emit('delTodo', todoItem.id)" />
    </div>
  </div>
</template>

<script>
import Item from "./Item.vue";

export default {
  name: "Items",
  props: ["todosList"],
  components: { Item },
  methods: {
    clicked() {
      //console.log(this.todosList.id);
    },
  },
};
</script>

<style>
</style>