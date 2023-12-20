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
    someObject: {
      handler(newValue, oldValue) {
				console.log(newValue, oldValue)
      },
			// watch is shallow by default: the callback will only trigger when the watched property has been assigned a new value
			// it won't trigger on nested property changes.
			// If you want the callback to fire on all nested mutations,
			// you need to use a deep watcher
			// this is expensive so use it when u don't know any other way
			deep: true
    }
  }
};
</script>
