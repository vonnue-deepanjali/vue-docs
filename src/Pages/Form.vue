<template>
    <form @submit.prevent="handleSubmit">
      <div>
        <label>Name:</label>
        <input type="text" v-model="name" />
      </div>
      <div>
        <label>Email:</label>
        <input type="email" v-model="email" />
      </div>
      <div>
        <label>Password:</label>
        <input type="password" v-model="password" />
      </div>
      <button type="submit">Submit</button>
    </form>

</template>
  
<script setup>

  import { ref } from 'vue'
  
  const name = ref('')
  const email = ref('')
  const password = ref('')
  
  function handleSubmit() {
    console.log('Name:', name.value)
    console.log('Email:', email.value)
    console.log('Password:', password.value)
  }
  
</script>
  