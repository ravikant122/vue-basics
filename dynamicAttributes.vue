<script>
export default {
  data() {
    return {
      attributeName: 'href',
      url: 'https://github.com/'
    }
  }
}
</script>

<template>
  <!-- Dynamic Arguments
  similarly we can pass events @eventName (eventName can be data or computed prop)

  these dynamic arguments can only be string/null otherwise it will throw warning

  we cannot do like this: 'foo' + attriuteName - so its better to have it as data or computed prop
  -->
  <a :[attributeName]="url"> GitHub</a>
</template>
