<!-- 父组件 ParentComp.vue -->
<template>
  <ChildComp
    :cntname="myName"
    @update:cntname="handleUpdate"
  />
  {{ myName}}
</template>
 
<script setup>
import {ref} from "vue"
import ChildComp from './ChildComp.vue';
let myName = ref("Vue 框架")
function handleUpdate(newName) {
  myName.value = newName
}
</script>
