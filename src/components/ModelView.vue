<template>
  <div>
    <CustomInput v-model:title="pageTitle" />
    <h3>输入的实时内容：{{ pageTitle }}</h3>
  </div>
</template>

<script>
import CustomInput from './CustomInput.vue';

export default {
  components: {
    CustomInput
  },
  data() {
    return {
      pageTitle: 'Hello, World!'
    }
  }
}
</script>
