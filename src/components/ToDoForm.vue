<template>
  <form @submit.prevent="requestAdd">
    <input
      type="text"
      id="newTodo"
      placeholder="New To-do"
      v-model="formData"
    />
  </form>
</template>

<script>
export default {
  name: "ToDoForm",
  data(){
    return {
        formData: ''
    } 
  }
};
</script>
