<template>
  <label class="checkbox" v-bind:class="{ 'is-complete' : todo.completed }">
    <input type="checkbox" v-on:click=markComplete(todo)>
    {{ todo.title }}
  </label>  
</template>


<script>

export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete(todo) {
      todo.completed = !todo.completed;
      console.log(todo.completed);
    }
  }
}

</script>


<style lang="scss" scoped>
  .is-complete {
    text-decoration: line-through;
  }
</style>