<template>
<div>
    <h2>Timer: {{ seconds }} seconds</h2>
</div>
</template>

<script setup>
import { ref, onMounted, onUpdated, onUnmounted } from 'vue';

const seconds = ref(0);
let interval = null

onMounted(() => {
    console.log('Componenet mounted');
    interval = setInterval(() => {
        seconds.vallue++;
    }, 1000);
})

onUpdated(() => {
    console.log(`Component is updated: seconds = ${seconds.value}`);
})

onUnmounted(() => {
    console.log('Component unmounted, timer cleared');
    clearInterval(interval)
})

</script>