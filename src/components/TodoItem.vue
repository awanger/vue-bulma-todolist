<template>
  <label class="checkbox" v-bind:class="{ 'is-complete' : todo.completed }">
    <input type="checkbox" v-on:click=markComplete(todo)>
    {{ todo.title }}
    <div class="delete" v-on:click="$emit('delete-todo', todo)">X</div>
  </label>
</template>


<script>

export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete(todo) {
      todo.completed = !todo.completed;
    },
    removeTodo(todo) {
      // pass the todo that needs to be deleted
      console.log(todo);
    }
  }
}

</script>


<style lang="scss" scoped>
  .is-complete {
    text-decoration: line-through;
  }
  
  label {
    width: 100%;
  }

</style>