<template>
  <div>
    <ul v-for="(todo, i) in todoList"
        :key="i"
        class="list">
      <li>
        <span class="to-do-item">
          <i class="fas fa-times-circle delete-button" @click="requestDelete(i)"></i>
          <span 
            contenteditable="true"
            ref="todo"
            @blur="requestUpdate('todo', i)">
            {{todo}} 
          </span>
        </span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ToDoList",
  props: ['todoList'],
  methods: {
    requestDelete: function(index){
      this.$emit('deleteTodo', index)
    },
    requestUpdate: function(todoRef, i){
      this.todoList[i] = this.$refs[todoRef][i].innerText
    }
  }
};
</script>

<style>
.delete-button{
  color: #ec1212;
  cursor: pointer;
  margin-right: 8px;
}

.list{
  list-style-type: none;
  padding-left: 10px;
}

.to-do-item{
  font-size: 1.5rem;
}
</style>