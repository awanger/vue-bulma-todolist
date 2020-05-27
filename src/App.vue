<template>
  <div id="app">
    <JesusLama/>
  </div>
</template>

<script>

import JesusLama from './components/Todos.vue'

export default {
  name: 'App',
  components: {
    JesusLama
  },
  data() {
    return {
      shit: true
    }
  }
}
</script>

<style>

</style>
