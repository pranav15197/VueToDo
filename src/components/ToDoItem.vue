<template>
  <li :class="{'bottom-border': !noBottomBorder}">
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
    },
    noBottomBorder: {
      name: "noBottomBorder",
      type: Boolean,
      default: false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
li{
  padding: 15px 15px;
}
.bottom-border{
  border-bottom: 1px solid black;
}
</style>
