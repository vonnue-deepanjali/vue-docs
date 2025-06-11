<template>
  <button @click="state.count++">
    {{ count }}
  </button>
</template>

<script setup>
import { reactive, computed } from 'vue'

const state = reactive({
  count: 0,
})

const count = computed(() => state.count)
</script>
