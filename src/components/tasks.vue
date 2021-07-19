<template>
  <div :key="task.id" v-for="task in tasks">
    <Task @delete-task="$emit('delete-task', task.id)" :task="task" />
  </div>
</template>

<script>
import Task from "./task.vue";
export default {
  name: "tasks",
  props: {
    tasks: Array,
  },
  components: {
    Task,
  },
  emits: ["delete-task"],
};
</script>
