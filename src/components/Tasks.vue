<template>
  <div>
    <div
      v-for="task in tasks"
      :key="task.id"
    >
      <Task
        :task="task"
        @toggle-reminder="$emit('toggle-reminder', task.id)"
        @delete-task="$emit('delete-task', task.id)"
      />
    </div>
  </div>
</template>

<script>
import Task from './Task'
export default {
  name: 'Tasks',
  components: {
    Task
  },
  props: {
    tasks: {
      type: Array,
      default: []
    }
  },
  emits: ['delete-task', 'toggle-reminder'] // this is to remove the warning
}
</script>
