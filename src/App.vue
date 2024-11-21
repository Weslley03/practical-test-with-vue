<template>
  <h1>Hello World!</h1>
  <input 
    type="text"
    placeholder="digite aqui sua tarefa!"
    v-model="newTask"
  />
  <button @click="addTask"> add task! </button>
  <ul>
    <li v-for="task in tasks" :key="task[0]">  
      <span> {{ task[0] }} </span>
      <button @click="delTask(task[0])"> deletar </button>
    </li>
  </ul>
</template>
<script>
export default {
  
  data() {
    return {
      newTask:'',
      tasks: new Map(),
    };
  },  
  
  methods: {
    addTask() {
      if(this.newTask.length > 0) {
        this.tasks.set(Date.now(), this.newTask);
      };
      this.newTask = '';
    },
    delTask(taskId) {
      this.tasks.delete(taskId);
    },
  },
};
</script>
