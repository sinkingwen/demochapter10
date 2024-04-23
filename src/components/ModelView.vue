<!-- <template>
  <div>
    <CustomInput v-model:title="pageTitle" />
    <h3>输入的实时内容：{{ pageTitle }}</h3>
  </div>
</template>

<script setup>
import CustomInput from './CustomInput.vue';
import {ref } from 'vue'

const pageTitle = ref('Hello, World')
</script> -->

<!-- 父组件ModelView.vue -->
<script setup>
import { ref } from 'vue'
import CustomInput from './CustomInput.vue'
  
const title = ref('Hello, World')
</script>

<template>
  <CustomInput v-model="title" />
  <!-- <CustomInput v-model:title="title" /> -->
  <h1>{{ title }}</h1>
</template>