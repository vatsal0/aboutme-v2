<template>
	<v-container fluid style="min-height:100vh; width: 100%" id="projects">
		<h1 class="text-center">Projects</h1>

		<div class="d-flex flex-md-row flex-column flex-wrap justify-center">
			<v-card
				v-for="(item, i) in items"
				:key="i"
				dark
				class="my-4 pa-2 d-flex flex-column justify-space-between mx-md-4 mx-auto"
				:width="$vuetify.breakpoint.md ? '100%' : '20rem'"
			>
				<div class="text-md-left text-center">
					<p class="text-h6 font-weight-medium">
						{{item.title}}
					</p>

					<p class="text-subtitle">
						{{item.desc}}
					</p>
				</div>

				<v-card-actions class="text-md-left text-center">
					<v-btn 
						:href="item.source"
						target="_blank"
						color="orange lighten-2"
						text
						class="mx-md-0 mx-auto"
					>
						Source Code
					</v-btn>
				</v-card-actions>
			</v-card>
		</div>
	</v-container>
</template>

<script>
export default {
	data() {
		return {
			items: [
				{
					title: "Tutoring website",
					desc: "soon.",
					source: "",
				},
				{
					title: "National Park Service Info",
					desc: "Static Vue.js application for searching and filtering parks from\
					the National Park Service API based on tourist activities.",
					source: "https://github.com/vatsal0/national-parks",
				},
				{
					title: "Plannet",
					desc: "Node.js and jQuery application enabling groups of friends to\
					efficiently plan hangouts together.",
					source: "https://github.com/vatsal0/Plannet",
				},
			]
		}
	}
}
</script>
