<template>
  <div>
    <h2>Timer: {{ seconds }} seconds</h2>
  </div>
</template>

<script setup>
import { ref, onMounted, onUpdated, onUnmounted } from 'vue'

const seconds = ref(0)
let interval = null

onMounted(() => {
  interval = setInterval(() => {
    seconds.vallue++
  }, 1000)
})

onUpdated(() => {})

onUnmounted(() => {
  clearInterval(interval)
})
</script>
