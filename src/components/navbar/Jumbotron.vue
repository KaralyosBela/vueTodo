<template>
  <div class="jumbotron jumbotron-fluid mb-0">
    <div class="container text-center">
      <h1 class="display-4">{{ title }}</h1>
      <p class="lead">My first SPA with Vue.js!</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "navJumbotron",
  data() {
    return {
      title: "Todo list",
    };
  },
};
</script>

<style>
</style>