<template>
  <form @submit.prevent="requestAdd">
    <input
      type="text"
      id="to-do-form"
      placeholder="Add a new To-do"
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
  },
  methods:{
    requestAdd: function(){
      this.$emit('addTodo', this.formData)
      this.formData = ''
    }
  }
};
</script>

<style>
#to-do-form{
  margin: 10px;
  margin-top: 0;
  font-size: 1.5rem;
}
</style>