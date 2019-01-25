<template>
  <ul>
   <to-do-item v-for="(task, index) in tasks" :key="index" :task="task" :no-bottom-border="index == tasks.length-1"/>
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
  border: 2px solid gray;
  padding: 0px;
  border-radius: 10px;
  list-style: none;
}
</style>
