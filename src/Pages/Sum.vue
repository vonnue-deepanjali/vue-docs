<template>
  <p>Numbers: {{ data.numbers.join(', ') }}</p>
  <p>Sum: {{ total }}</p>
</template>

<script setup>
import { reactive, computed } from 'vue'

const data = reactive({
  numbers: [10, 20, 30, 40],
})

const total = computed(() => data.numbers.reduce((sum, num) => sum + num, 0))
</script>
