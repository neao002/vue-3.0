<template>
  <div :key="task.id" v-for="task in tasks">
    <Task :task="task" />
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
};
</script>
