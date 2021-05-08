<template>
  <button
    :style="{ background: color }"
    class="btn"
    @click="onClick"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    text: {
      type: String,
      default: 'Button Text'
    },
    color: {
      type: String,
      default: 'green'
    }
  },
  methods: {
    onClick () {
      console.log('click')
    }
  }
}
</script>
