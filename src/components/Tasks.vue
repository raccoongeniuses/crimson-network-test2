<template>
  <div>
    <div :key="task.id" v-for="task in tasks">
      <Task @delete-task="$emit('delete-task', task.id)" :task="task" />
      <h3>{{ task.text }}</h3>
    </div>
  </div>
</template>

<script>
import Task from "./Task";
export default {
  name: "TasksComponent",
  props: {
    tasks: Array,
  },
  components: {
    Task,
  },
  emits: ["delete-task"],
};
</script>
