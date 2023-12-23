<script>
import MyComponent from "./MyComponent.vue";

export default {
  components: { MyComponent },
  data() {
    return {
      title: "v-model argument example",
    };
  },
};
</script>

<template>
  <h1>{{ title }}</h1>
  <MyComponent v-model:title="title" />
</template>
