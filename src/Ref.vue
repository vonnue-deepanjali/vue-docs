<template>
    <button @click="state.count++">
      {{ state.count }}

    </button>
</template>

<script setup>
import { reactive } from 'vue'

const state = reactive({ count: 0})
// const count = ref(0)

// console.log(count)
// console.log(count.value)

// count.value++
// console.log(count.value)
</script>