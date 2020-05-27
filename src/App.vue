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
          <a>Incomplete</a>
          <a>Complete</a>
        </a>
      </div>
    </div>
  </div>
</template>

<script>

// import Todos from './components/Todos.vue'
import Search from './components/Search.vue'


export default {
  name: 'App',
  components: {
    Search
    // Todos
  },
  data() {
    return {
      shit: true
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
