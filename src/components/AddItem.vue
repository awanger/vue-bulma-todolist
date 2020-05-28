<template>
  <div class="panel-block">
    <p class="control has-icons-left">
      <input class="input" type="text" placeholder="Add new item">
      <span class="icon is-left">
        <i class="fas fa-search"></i>
      </span>
    </p>
  </div>
</template>

<script>
  export default {
    name: 'AddItem'
  }
</script>


<style lang="scss" scoped>
  .input {
    padding: 0;
    margin: 0;
    border: none;
  }

</style>