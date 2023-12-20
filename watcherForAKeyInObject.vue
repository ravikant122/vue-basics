<template>
	<div v-text="someObject" />
	<button @click="changeFirstName('asdf')" v-text="changeFirstNameString"  />
	<button @click="changeLastName('asdf')" v-text="changeLastNameString" />
	<button @click="changeName({ firstName: 'asdf', lastName: 'oiuo' })" v-text="changeNameString" />
</template>

<script>
export default {
	data () {
		return {
			someObject: {
				firstName: 'ravi',
				lastName: 'kant'
			},
			changeFirstNameString: 'Change First Name',
			changeLastNameString: 'Change Last Name',
			changeNameString: 'Change Name'
		}
	},

	methods: {
		changeFirstName (firstName) {
			this.someObject.firstName = firstName
		},
		changeLastName (lastName) {
			this.someObject.lastName = lastName
		},
		changeName (newName) {
			this.someObject = newName
		}
	},

  watch: {
    // this will set watcher only for firstName in someObject - means a particular key in an Object
    'someObject.firstName' (newValue) {
			console.log(newValue)
    }
  }
};
</script>
