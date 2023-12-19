<script>
export default {
  data() {
  	return {
	    myObject: {
  	    title: 'How to do lists in Vue',
	      author: 'Jane Doe',
      	publishedAt: '2016-04-10'
    	}
  	}
	}
}
</script>

<template>
	<ul>
		<!-- it will only display the values -->
		<li v-for="value in myObject">
			{{ value }}
		</li>
	</ul>
	<ul>
		<li v-for="(value, key) in myObject">
			{{ key }}: {{ value }}
		</li>
	</ul>
	<ul>
    <li v-for="(value, key, index) in myObject">
		  {{ index }}. {{ key }}: {{ value }}
		</li>
  </ul>
</template>
