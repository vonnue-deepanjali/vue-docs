<template>
  <ul v-for="numbers in sets">
    <li v-for="n in even(numbers)">{{ n }}</li>
  </ul>
</template>

<script setup>
import { ref } from 'vue'

const sets = ref([
  [1, 2, 3, 4, 5],
  [6, 7, 8, 9, 10],
])

function even(numbers) {
  return numbers.filter((number) => number % 2 === 0)
}
</script>
