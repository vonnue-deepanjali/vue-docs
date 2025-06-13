<template>
    <div v-show="contents">Items</div>
    <div v-if="type === 'A'">{{ type }} - Apple</div>
    <div v-else-if="type === 'B'">{{ type }} - Berry</div>
    <div v-else-if="type === 'C'">{{ type }} - Carrot</div>
    <div v-else="type">Nothing is available related to this {{ type }}</div>
</template>

<script setup>
import { ref } from 'vue'

const type = ref('A')
const contents = ref(true)

</script>