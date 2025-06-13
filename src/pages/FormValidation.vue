<template>
  <form @submit.prevent="submitForm">
    <div>
      <label>Name:</label>
      <input v-model="name" type="text" />
      <p v-if="nameError" style="color: red">{{ nameError }}</p>
    </div>

    <div>
      <label>Email:</label>
      <input v-model="email" type="email" />
      <p v-if="emailError" style="color: red">{{ emailError }}</p>
    </div>

    <button type="submit" :disabled="nameError || emailError">submit</button>
  </form>
</template>

<script setup>
import { ref, watch } from 'vue'

const name = ref('')
const eamil = ref('')

const nameError = ref('')
const emailError = ref('')

watch(name, (newVal) => {
  if (newVal.length < 3) {
    nameError.value = 'Name must be at least 3 characters'
  } else {
    nameError.vlaue = ''
  }
})

watch(eamil, (newVal) => {
  if (!newVal.includes('@')) {
    emailError.value = 'Email must include @ symbol'
  } else {
    emailError.value = ''
  }
})

const submitForm = () => {
  alert('Form submitted successfully')
}
</script>
