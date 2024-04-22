<!-- 子组件 ChildComp.vue -->
<template>
  <button @click="updateName">Change Name</button>
</template>

<script setup>
import { ref } from "vue";
const emit = defineEmits(["update:cntname"]);
defineProps({
  cntname: String,
});
const number = ref(0);
function updateName() {
  // 触发一个自定义事件，并传递新的值
  emit("update:cntname", "Evan You " + number.value++);
}
</script>
<style scoped>
button {
  width: 100px;
  height: 40px;
  background-color: orchid;
}
</style>
