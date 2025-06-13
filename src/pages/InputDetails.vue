<template>
  <div>
    <h2>Enter your name:</h2>
    <MyInput v-model="name" placeholder="Type your name here..." />
    <p>
      You entered: <strong>{{ name }}</strong>
    </p>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import MyInput from '@/components/MyInput.vue';

const name = ref('')
</script>
