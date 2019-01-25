<template>
  <ul>
   <to-do-item v-for="(task, index) in tasks" :key="index" :task="task"/>
  </ul>
</template>

<script>
import ToDoItem from './ToDoItem.vue'
export default {
  name: 'ToDoList',
  props: {
    tasks: {
      name: "tasks",
      type: Array
    }
  },
  components: {
    ToDoItem
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  border: 1px solid black;
  border-radius: 10px;
  padding: 20px;
  list-style: none;
}
</style>
