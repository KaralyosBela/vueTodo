<template>
  <div>
    <div class="progress">
      <div
        class="progress-bar bg-success"
        role="progressbar"
        style="width: 25%"
        aria-valuenow="25"
        aria-valuemin="0"
        aria-valuemax="100"
      >
        25%
      </div>
    </div>
    <nav class="navbar navbar-dark bg-dark">
      <span class="navbar-brand mb-0 h1"> {{ title }} </span>

      <form class="form-inline">
        <div class="form-group mr-sm-2">
          <input type="text" class="form-control " />
        </div>

        <button type="button" class="btn btn-primary mr-sm-2">Add</button>

        <button type="button" class="btn btn-success mr-sm-2">
          Todos done
          <span class="badge badge-light">{{
            todosList.filter((obj) => obj.completed).length
          }}</span>
        </button>

        <button type="button" class="btn btn-danger">
          Todos remaining
          <span class="badge badge-light">{{
            todosList.filter((obj) => !obj.completed).length
          }}</span>
        </button>
      </form>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Navbartodo",
  props: ["todosList"],
  components: {},
  data() {
    return {
      title: "Todo list",
      todosRemaining: 10,
      todosDone: 0,
    };
  },
  methods: {},
};
</script>

<style>
</style>