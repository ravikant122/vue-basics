<script>
export default {
  // we cannot use some other name in this prop becuase v-model has fixed name for its prop that is modelValue
  props: ['modelValue'],
  emits: ['update:modelValue']
}
</script>

<template>
  <input
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
  />
</template>