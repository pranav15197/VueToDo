<template>
  <div class="main">
    <h1>To Do</h1>
    <input v-model="newTask" />
    <button @click="addTask">Add Task</button>
   <to-do-list :tasks="tasks"/>
  </div>
</template>

<script>
import ToDoList from './ToDoList.vue'
export default {
  name: 'Main',
  components: {
    ToDoList
  },
  data:()=>{
    return {
      newTask: "",
      tasks: []
    }
  },
  methods: {
    addTask(){
      if(this.newTask === ""){
        alert("Task cannot be empty!");
      }else{
        this.tasks.push(this.newTask);
        this.newTask = ""
      }
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
