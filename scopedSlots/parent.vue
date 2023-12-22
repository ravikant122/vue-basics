<script>
import MyComponent from "./MyComponent.vue";

export default {
  components: {
    MyComponent,
  },
};
</script>

<template>
  <!-- slots can't access childs dat but there's a way - we can use slot props
    its like we'll give props to the slots in child component and slot is then use the those
    props in parent component, since the props in slot are being in child it can use childs data

    here slotPropsss = props object given in slot in child component
  -->
  <MyComponent v-slot="slotPropsss">
    {{ slotPropsss.text }} -- {{ slotPropsss.count }}
  </MyComponent>
</template>
