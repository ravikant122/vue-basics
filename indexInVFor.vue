<script>
export default {
  data() {
  	return {
    	items: [{ message: 'Foo' }, { message: 'Bar' }]
  	}
	}
}
</script>

<template>
	<!-- you can always index, vue will give you that -->
	<li v-for="(item, index) in items">
  	{{ index }} - {{ item.message }}
	</li>
</template>
