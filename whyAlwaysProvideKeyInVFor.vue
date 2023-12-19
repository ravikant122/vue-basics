<template>
  <template v-for="people in names">
    <h2>{{ people.name }}</h2>
    <input placeholder="Last name" />
    <hr />
  </template>
  <button @click="shuffle">Shuffle!</button>

	<!-- when we shuffle the names then only names gets shuffled and their input remains the same
	because the default behavior of v-for will try to patch the elements in-place without moving them.
	meaning it will only changes the name in DOM not the whole node
	-- this is why we have to always provide :key attribute in v-for
	-- there are two ways to provide something in key
		1. index of v-for
		2. some id in the data(can be anything like number, string but all should be diff)

		for 1 (index of v-for) we can't use this since it always increase gradually
		means no matter the node, the first node always gets key as 0, second node as 1 and so on
		because index of vue will be fresh everytime it gets compiled

		for 2 - it works because the it's related to data
	-->

	<template v-for="people in names" :key="people.id">
    <h2>{{ people.name }}</h2>
    <input placeholder="Last name" />
    <hr />
  </template>
  <button @click="shuffle">Shuffle!</button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      names: [{ name: "Bruce", id: 0 }, { name: "Clark", id:1 }, { name: "Diana", id: 2 }, { name: "Berry", id:3 }]
    };
  },
  methods: {
    shuffle() {
      this.names = [this.names[2],this.names[0],this.names[3],this.names[1]];
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
