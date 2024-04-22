<template>
  <div>
    <input :value="title" @input="handleInput" />
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: ''
    }
  },
  emits: ['update:title'],
  methods: {
    handleInput(event) {
      this.$emit('update:title', event.target.value);
    }
  }
}
</script>
<style scoped>
input{
  width: 200px;
  height: 30px;
}
</style>