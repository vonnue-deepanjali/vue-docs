<template>
<div>
    <input ref="nameInput" type="text" placeholder="Enter your name" />
    <button @click="focusInput">Focus Input</button>
</div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const nameInput = ref(null);

onMounted(() => {
    nameInput.value.focus();
});

const focusInput = () => {
    nameInput.value.focus();
};

</script>