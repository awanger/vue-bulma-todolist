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
        <todos v-bind:todos="todos" /> <!-- pass an array -->
        <add-item v-on:click='addTodo'/>
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
          completed: true
        },
        {
          id:3,
          title: "Third Todo",
          completed: false
        },
        {
          id:4,
          title: "Fourth Todo",
          completed: true
        },
        {
          id:5,
          title: "Fifth Todo",
          completed: true
        }
      ]
    }
  },
  methods: {
    addTodo(newTodo) {
      this.todos = [...this.todos, newTodo];
      console.log("hello world");
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
