<template>
  <div id="app">
    <div class="container">
      <div class="panel">
        <p class="panel-heading">
          Todo List
        </p>
        <search/>
        <a class="panel-tabs">
          <a class="is-active">All</a>
          <a>Complete</a>
          <a>Incomplete</a>
        </a>
        <todos v-on:delete-todo='removeTodo' v-bind:todos="todos" /> <!-- pass an array -->
        <add-item v-on:create-todo='addTodo'/>
      </div>
    </div>
  </div>
</template>

<script>

import Todos from './components/Todos.vue'
import Search from './components/Search.vue'
import AddItem from './components/AddItem.vue'


export default {
  name: 'App',
  components: {
    Search,
    Todos,
    AddItem
  },
  data() {
    return {
      todos: [
        {
          id:1,
          title: "First Todo",
          completed: false
        },
        {
          id:2,
          title: "Second Todo",
          completed: false
        },
        {
          id:3,
          title: "Third Todo",
          completed: false
        },
        {
          id:4,
          title: "Fourth Todo",
          completed: false
        },
        {
          id:5,
          title: "Fifth Todo",
          completed: false
        }
      ]
    }
  },
  methods: {
    addTodo(newTodo) {
      // add todo to the list
      this.todos = [...this.todos, newTodo];
    },
    removeTodo(todo) {
      var index = this.todos.indexOf(todo);
      if(index > -1) {
        this.todos.splice(index, 1);
      }
    }
  }
}
</script>

<style lang="scss">
  @import './../node_modules/bulma/css/bulma.css';

  .container {
    margin-top: 4rem;
    max-width: 800px;
  }

  $some-variable: red;

  h1 {
    color: $some-variable;
  }
</style>
