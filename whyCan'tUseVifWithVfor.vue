<script>
export default {
  data() {
  	return {
	    todos: [
				{
					name: 'ravi',
					isCompleted: true
				},
				{
					name: 'abhi',
					isCompleted: false
				}
			]
  	}
	}
}
</script>

<template>
	<ul>
		<li v-for="todo in todos" v-if="todo.isCompleted"> <!-- this lines gives error -->
			{{ todo.name }}
		</li>
		<!-- v-if has higher precendence than v-for that's why v-if can't access the variables of v-for -->
	</ul>
</template>
