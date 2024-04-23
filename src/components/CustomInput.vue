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
// defineModel() 返回的值是一个 ref,
// 作用是在父组件和当前变量之间进行双向绑定
const title = defineModel()
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

<!-- 组件上的 v-model 也可以接受一个参数 -->
<!-- <script setup>
// defineModel() 返回的值是一个 ref,
// 作用是在父组件和当前变量之间进行双向绑定
const title = defineModel('title')
</script>

<template>
  <input type="text" v-model="title" />
</template> -->