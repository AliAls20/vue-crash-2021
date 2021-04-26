<template>
  <div v-for="task in tasks" :key="task.id">
    <Task :task="task" />
  </div>
</template>

<script>
import Task from "./Task";
export default {
  name: "Tasks",
  props: {
    tasks: {
      type: Array,
      default: [],
    },
  },
  components: {
    Task,
  },
};
</script>
