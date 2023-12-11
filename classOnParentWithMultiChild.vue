<script setup></script>

<template>
  <!-- when parent has multiple childs
  then style given to parent won't be applicable to all the children
  so each child needs to use the style by itself
  -->
  <p :class="$attrs.class">Hi</p>
  <span>This is a child component</span>
  <p>
    <span :class="$attrs.class">Hi</span>
  </p>
</template>
