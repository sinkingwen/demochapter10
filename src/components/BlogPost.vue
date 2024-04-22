<script setup>
import { ref } from 'vue'
defineProps({
  title: {
    type: String,
    required: true,
    default:'Blog 1'
  }
})
const emit = defineEmits(['enlarge-text','update-title'])
function change() {
  emit('update-title')
}
function handleEnlargeText() {
  emit('enlarge-text')
}
</script>

<template>
  <h1 @click="handleEnlargeText">{{ title }}</h1>
  <button @click="change">Update Title</button>
</template>
<style scoped>

button{
  width: 100px;
  height: 40px;
  background-color: rgb(93, 181, 194);
}</style>