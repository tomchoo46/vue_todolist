<template>
  <div id="app">
    <h1>To-do-list (Vue.js)</h1>
    <to-do-form @addTodo='addTodo'></to-do-form>
    <to-do-list :todoList="todoList" @deleteTodo='deleteTodo'>
    </to-do-list>
  </div>
</template>

<script>
import ToDoForm from './components/ToDoForm.vue'
import ToDoList from './components/ToDoList.vue'

export default {
  name: 'app',
  data(){
    return{
      todoList: ['todo3', 'todo2', 'todo1']
    }
  },
  components: {
    "to-do-form": ToDoForm,
    "to-do-list": ToDoList
  },
  methods:{
    addTodo: function(todo){
      this.todoList.unshift(todo)
    },
    deleteTodo: function(index){
      this.todoList.splice(index, 1)
    }
  }
}
</script>
