<script setup>
import { ref } from "vue"
let count = ref(0)
</script>
<template>
    <button @click="count++">Count: {{ count }} times</button>

</template>
<style scoped>
button{
  width: 100px;
  height: 40px;
  background-color: rgb(148, 184, 148);
}
</style>