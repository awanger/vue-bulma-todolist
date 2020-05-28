<template>
  <div id="todos">
    <div class="panel-block" v-for="todo in todos" v-bind:key="todo.id">
      <todo-item v-bind:todo="todo"/>
    </div>
  </div>

</template>

<script>

import TodoItem from "./TodoItem";

export default {
  name: 'Todos',
  components: { TodoItem },
  props: { todos: Array }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  #todos {
    width: 100%;
    margin: 0;
    padding: 0;
  }
</style>
