<template>
  <div v-for="task in tasks" :key="task.id">
    <Task @delete-task="$emit('delete-task', task.id)" :task="task" />
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
  emits: ["delete-task"], // this is to remove the warning
};
</script>
