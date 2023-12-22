<script>
export default {
  data() {
    return {
      greetingMessage: "hello",
    };
  },
};
</script>

<template>
  <div>
    <slot name="header" :text="greetingMessage" :count="1"></slot>
  </div>
</template>
