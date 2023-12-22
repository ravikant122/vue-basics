<script>
import MyComponent from "./MyComponent.vue";

export default {
  components: {
    MyComponent,
  },
};
</script>

<template>
  <!-- for 1st slot, headerProps = props object given in MyComponent
  -->
  <MyComponent>
    <template #header="headerProps">
      {{ headerProps }}
    </template>

    <template #default="defaultProps">
      {{ defaultProps }}
    </template>

    <template #footer="footerProps">
      {{ footerProps }}
    </template>
  </MyComponent>
</template>
