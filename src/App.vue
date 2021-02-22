<template>
  <div id="app">
    <navJumbotron />
    <Navbartodo v-bind:todosList="todosList" />
    <Items v-bind:todosList="todosList" v-on:delTodo="deleteTodo" />
  </div>
</template>

<script>
import Navbartodo from "./components/navbar/Navbar.vue";
import navJumbotron from "./components/navbar/Jumbotron.vue";
import Items from "./components/Body/Items.vue";

export default {
  name: "App",
  data() {
    return {
      todosList: [
        {
          id: 1,
          title: "Cleaning the room",
          completed: false,
        },
        {
          id: 2,
          title: "Buy soap",
          completed: false,
        },
        {
          id: 3,
          title: "Eat the soap",
          completed: false,
        },
      ],
    };
  },
  components: {
    Navbartodo,
    navJumbotron,
    Items,
  },
  methods: {
    deleteTodo(id) {
      this.todosList = this.todosList.filter((x) => x.id !== id);
    },
  },
};
</script>

<style>
</style>
