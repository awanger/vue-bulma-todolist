<template>
  <div class="panel-block">
    <p class="control has-icons-left">
      <input class="input" type="text" placeholder="Add new item"
             v-model="inputText"
             v-on:change="createTodo(inputText)">
      <span class="icon is-left">
        <i class="fas fa-search"></i>
      </span>
    </p>
  </div>
</template>

<script>

  import { v4 as uuidv4 } from 'uuid';
  export default {
    name: 'AddItem',
    data() {
      return {
        inputText: ""
      }
    },
    methods: {
      clearInputText() {
        this.inputText = "";
      },
      createTodo(inputText) {
        // create new todo object
        const newTodo = {
          id: uuidv4(),
          title: inputText,
          completed: false
        }
        console.log(newTodo);
        // send up to parent component
        this.$emit('create-todo', newTodo);
        this.clearInputText();
      }
    }
  }
</script>


<style lang="scss" scoped>
  .input {
    padding: 0;
    margin: 0;
    border: none;
  }
</style>