<template>
	<v-container fluid style="min-height:100vh; width: 100%" id="experience">
		<h1 class="text-center">Experience</h1>

		<div>
			<v-timeline :dense="dense">
				<v-timeline-item
					v-for="(item, i) in items"
					:key="i"
				>
					<template v-slot:icon>
						<v-avatar>
							<img :src="item.img">
						</v-avatar>
					</template>

					<v-card class="elevation-2">
						<p class="text-h4 pt-2 pb-0 ml-4">{{item.title}}</p>
						<p class="overline py-0 ml-4 mb-0">{{item.time}}</p>

						<v-card-text class="pt-2">
							<v-list-item
							v-for="(line, i) in item.desc"
							:key="i">
								<v-list-item-content>
									<v-list-item-title class="text-wrap">{{line}}</v-list-item-title>
								</v-list-item-content>
							</v-list-item>
						</v-card-text>
					</v-card>
				</v-timeline-item>
			</v-timeline>
		</div>
	</v-container>
</template>

<script>
export default {
	data() {
		return {
			items: [
				{
					time: "Nov 2021 - Present",
					title: "Research Assistant",
					place: "University of Maryland",
					desc: ["Working under Dr. Lars Olson in the Department of Agriculture and Resource Economics.",
						"Utilizing a web scraper to collect invasive species data from the CABI Invasive Species Compendium.",
						"Developing a natural language processing model to extract insights related to the economic impact of\
						invasive species and identify the most prominent economic threats."],
					img: "https://osc.umd.edu/img/logos/28_informalseal.jpg"
				},
				{
					time: "Sep 2020 - Aug 2021",
					title: "Software Engineer Intern",
					place: "Bloomberg LP",
					desc: ["Developed a RESTful service using Java and Spring Framework to\
					manage over 900 permissions and settings used by the Bloomberg Law web application.",
					"Created a responsive and dynamic interface with Vue.js, GraphQL, and\
					Ruby on Rails to communicate with the Java service via HTTP requests.",
					"Provided analytics allowing managers to recognize and remove hundreds\
					of unused permissions, reducing login time by over 200ms.",
					"Presented interface in front of managers and senior engineers to receive\
					feedback for implementing new features and improving user experience."],
					img: "https://www.logolynx.com/images/logolynx/57/5749ace331ebd85068ef14fcdc115285.jpeg"
				}
			]
		}
	},
	computed: {
		dense () {
			switch (this.$vuetify.breakpoint.name) {
				case 'xs': return true
				case 'sm': return true
				case 'md': return false
				case 'lg': return false
				case 'xl': return false
			}
		},
	}
}
</script>