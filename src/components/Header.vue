<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
      @btn-click="$emit('toggle-add-task')"
    />
  </header>
</template>

<script>
import Button from './Button'
export default {
  name: 'Header',
  components: {
    Button
  },
  props: {
    title: {
      type: String,
      default: 'Title Tracker'
    },
    showAddTask: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
