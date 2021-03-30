<template>
	<div id="nav">
		<router-link to="/">Home</router-link> |
		<router-link :to="{ name: 'Jobs' }">Jobs</router-link> |
		<router-link :to="{ name: 'About' }">About</router-link>
	</div>

	<button @click="redirect">Redirect</button>
	<button @click="back">Back</button>
	<button @click="forward">Forward</button>
	<router-view />
</template>

<script>
export default {
	methods: {
		redirect() {
			this.$router.push({ name: "Home" });
		},
		back() {
			this.$router.go(-1);
		},
		forward() {
			this.$router.go(1);
		},
	},
};
</script>

<style lang="sass">
@import "styles/global.sass"

button
	margin: 0 10px
	padding: 10px
	border: none
	border-radius: 4px
	cursor: pointer
	outline: none
</style>
