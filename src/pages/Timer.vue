<template>
  <div>
    <h2>Timer: {{ seconds }} seconds</h2>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const seconds = ref(0)
const interval = ref(null)

onMounted(() => {
  interval = setInterval(() => {
    seconds.value++
  }, 1000)
})

onUnmounted(() => {
  clearInterval(interval)
})
</script>