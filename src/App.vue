<template>
  <div id="app">
    <h1>To-do-list (Vue.js)</h1>
    <to-do-form></to-do-form>
  </div>
</template>

<script>
import ToDoForm from './components/ToDoForm.vue'

export default {
  name: 'app',
  components: {
    "to-do-form": ToDoForm
  }
}
</script>

<style>
</style>
