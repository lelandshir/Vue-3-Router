<template>
	<div class="about">
		<h1>Vue 3 Router Sandbox</h1>
		<h2>by {{ author.name }}, {{ author.role }}</h2>
	</div>
</template>

<script>
export default {
	data() {
		return {
			author: { name: "Léland Shirley", role: "Web Developer" },
		};
	},
};
</script>

<style lang="sass"></style>
