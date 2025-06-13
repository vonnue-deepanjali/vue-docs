<template>
  <input
    :placeholder="placeholder"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
  />
</template>

<script setup>
defineProps(['modelValue', 'placeholder'])
defineEmits(['update:modelValue'])
</script>
