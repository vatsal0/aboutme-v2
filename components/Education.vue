<template>
	<v-container fluid style="min-height:100vh; width: 100%" id="education">
		<h1 class="text-center">Education</h1>

		<div class="d-flex flex-md-row flex-column flex-wrap justify-center">
			<v-card
				v-for="(item, i) in items"
				:key="i"
				dark
				class="ma-4 pa-2"
			>
				<div class="d-flex flex-md-row flex-column-reverse flex-no-wrap text-md-left text-center" style="height: 100%">
					<div>
						<p class="text-h5 pa-4 ma-0">{{item.title}}</p>

						<v-card-subtitle class="overline pt-0" v-text="item.time"></v-card-subtitle>

						<v-card-text>
							<p class="text-h6 mb-0">{{item.descType}}:</p>
							<p
								v-for="(line, i) in item.desc"
								:key="i"
								class="caption my-2">
								{{line}}
							</p>
						</v-card-text>
					</div>

					<v-avatar
						class="my-auto mx-auto"
						size="10rem"
					>
						<v-img :src="item.img"></v-img>
					</v-avatar>
				</div>
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
					title: "Capital One Engineering Summit",
					time: "Jan 2021",
					img: "https://pbs.twimg.com/profile_images/1455173719027068929/I6ffWyrd_400x400.jpg",
					descType: "Workshops",
					desc: ["iOS Development",
					"React.js",
					"Postgres + PgAdmin"]
				},
				{
					title: "University of Maryland",
					time: "Aug 2021 - Present",
					img: "https://osc.umd.edu/img/logos/28_informalseal.jpg",
					descType: "Coursework",
					desc: ["Object Oriented Programming",
					"Linear Algebra",
					"Harvesting Big Data"]
				},
				{
					title: "Bergen County Academies",
					time: "Sep 2017 - Jun 2021",
					img: "https://bca-admissions.bergen.org/images/logo.png",
					descType: "Coursework",
					desc: ["AP Computer Science",
					"C & Data Structures",
					"Functional Programming",
					"Computational Theory",
					"Multivariable Calculus",
					"Web Development"]
				}
			]
		}
	}
}
</script>