<script>
import CustomInput from './CustomInput.vue'

export default {
  components: { CustomInput },
  data() {
    return {
      message: 'hello'
    }
  }
}
</script>

<template>
<!-- v-model can be expand into
  :modelValue="message" @update:modelValue="newValue => message = newValue"

  modelValue name is fixed, that's why we've to create a prop of name modelValue
-->
  <CustomInput v-model="message" /> {{ message }}
</template>