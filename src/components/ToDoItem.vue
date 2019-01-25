<template>
  <li>
   {{task}}
  </li>
</template>

<script>
export default {
  name: 'ToDoItem',
  props: {
    task: {
      name: "task",
      type: String
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
