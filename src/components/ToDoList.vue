<template>
  <div>
    <ul v-for="(todo, i) in todoList"
        :key="i">
      <li>{{todo}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ToDoList",
  props: ['todoList']
};
</script>
