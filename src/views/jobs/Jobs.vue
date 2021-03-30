<template>
	<h1>Jobs</h1>
	<div v-for="job in jobs" :key="job.id" class="job">
		<router-link
			:to="{
				name: 'JobDetails',
				params: { id: job.id },
			}"
		>
			<h2>{{ job.title }}</h2>
		</router-link>
	</div>
</template>

<script>
export default {
	data() {
		return {
			jobs: [
				{
					id: 1,
					name: "Darth Vader",
					title: "Technical Architect",
					details:
						"Making sure that Clients and the Creative Team have an intricate understanding of what the deliverables should be.",
				},
				{
					id: 2,
					name: "Léland Shirley",
					title: "Jr. Web Developer",
					details:
						"Building custom applications for the web. Assisting the Senior Developer on projects and supporting the Creative Team by bringing designs into fruition via code.",
				},
				{
					id: 3,
					name: "Mace Windu",
					title: "Sr. Web Developer",
					details:
						"Has a wealth of experience and understanding of the applications we build for the web. Leads developmenmt on most large scale projects. Mentor to Junior Developers.",
				},
				{
					id: 4,
					name: "Luke Skywalker",
					title: "Engagement Manager",
					details:
						"Bridges the gap between the Creative Team and the Client. Protects the Creatives from fierce requests and communictates details in a way everyone can understand. Translates the work of developers into plain English for clients.",
				},
			],
		};
	},
};
</script>

<style lang="sass">
.job h2
	background: #f4f4f4
	padding: 20px
	border-radius: 10px
	margin: 10px auto
	max-width: 600px
	cursor: pointer
	color: #000

.job h2:hover
	background: #ddd

.job a
	text-decoration: none
</style>
