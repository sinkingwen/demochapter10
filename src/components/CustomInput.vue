<!-- <template>
  <div>
    <input type="text" :value="title" @input="handleInput" />
  </div>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    default: "default title",
  },
});
const emit = defineEmits(["update:title"]);
function handleInput(event) {
  emit("update:title", event.target.value);
}
</script> -->

<!-- CustomInput.vue -->
<script setup>
const title = defineModel('title')
</script>

<template>
  <input type="text" v-model="title" />
</template>
<style scoped>
input {
  width: 200px;
  height: 30px;
}
</style>
