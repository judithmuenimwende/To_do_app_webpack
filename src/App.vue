<template>
  <div class="container">
    <h3>{{ title }}</h3>
    <form>
      <textarea placeholder="Add new task" v-model="newTask"></textarea>
      <p>{{newTask}}</p>
      <button type="button" v-on:click="addTask">Add Task {{clicked}}</button>
    </form>
    <ul>
   <li v-for="task in tasks">{{task}}</li>
    </ul>
    
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      title: 'To Do List',
      newTask:'This is a Judith',
      clicked: 0,
      tasks:[]
    }
  },
  methods: {
  	addTask(){
  	this.tasks.unshift(this.newTask);
  	this.newTask = '';
  	}
  }
}
</script>
