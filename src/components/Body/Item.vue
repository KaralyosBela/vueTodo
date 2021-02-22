<template>
  <div>
    <div class="list-group-item">
      <input class="form-check-input" type="checkbox" value="" />
      {{item.title}}
      <span></span>
      <button v-on:click="$emit('delTodo', item.id)" class="btn btn-outline-danger">Delete</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Item",
  props: ["item"],
  methods: {},
};
</script>

<style>
ol li {
  display: inline-block;
}
</style>