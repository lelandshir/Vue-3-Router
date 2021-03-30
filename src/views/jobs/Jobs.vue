<template>
	<h1>Jobs</h1>
	<div v-for="job in jobs" :key="job.id">
		<h2>{{ job.title }}</h2>
	</div>
</template>

<script>
export default {
	data() {
		return {
			jobs: [
				{
					id: 1,
					name: "Greg Vader",
					title: "UI Designer",
					details: "Building things for the web.",
				},
				{
					id: 2,
					name: "Léland Skywalker",
					title: "Jr. Web Developer",
					details: "Building things for the web.",
				},
				{
					id: 3,
					name: "Ed Windu",
					title: "Sr. Web Developer",
					details: "Building things for the web.",
				},
				{
					id: 4,
					name: "Sydney Skywalker",
					title: "Graphic Designer",
					details: "Building things for the web.",
				},
			],
		};
	},
};
</script>

<style lang="sass"></style>
