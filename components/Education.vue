<template>
	<v-container fluid style="min-height:100vh; width: 100%" id="education">
		<h1 class="text-center">Education</h1>

		<div class="d-flex flex-md-row flex-column flex-wrap justify-center">
			<v-card
				v-for="(item, i) in items"
				:key="i"
				dark
				class="my-4 pa-2 mx-md-4 mx-auto"
				max-width="25rem"
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
					img: "https://media.licdn.com/dms/image/C560BAQF0OgQyRZ9yAA/company-logo_200_200/0/1635782717682?e=1689811200&v=beta&t=vCzZLfWHxKAzN2pBQK4TwwM6MzRs3QCvkgYvasPUDXw",
					descType: "Skills",
					desc: ["iOS Development",
					"React.js",
					"Postgres + PgAdmin"]
				},
				{
					title: "Machine Learning (Stanford Online)",
					time: "Dec 2021",
					img: "https://media.licdn.com/dms/image/C4D0BAQE5MTWc9Bgf0g/company-logo_200_200/0/1582306984947?e=1689811200&v=beta&t=r5EvoS3MD3JvFv_k3BSNhNkaVoahl3Qz0h5fmXWspYQ",
					descType: "Skills",
					desc: ["Linear Regression",
					"Logistic Regression",
					"Neural Networks",
					"Support Vector Machines",
					"K-Means Clustering",
					"Principal Component Analysis",
					"Collaborative Filtering",
					"Hyperparameter Optimization"]
				},
				{
					title: "University of Maryland",
					time: "Aug 2021 - Present",
					img: "https://media.licdn.com/dms/image/C560BAQHrhLnmmZTGjQ/company-logo_200_200/0/1519856141972?e=1689811200&v=beta&t=eeCMS3LCo40aKQaOjDRFY4YoEle37OY4v0VUtISNj_o",
					descType: "Coursework",
					desc: ["Object Oriented Programming",
					"Linear Algebra",
					"Harvesting Big Data"]
				},
				{
					title: "Bergen County Academies",
					time: "Sep 2017 - Jun 2021",
					img: "https://media.licdn.com/dms/image/C4D0BAQGliYezbak3eg/company-logo_200_200/0/1519856877466?e=1689811200&v=beta&t=-6WC4VSHDZMKgQDgaeoxWRsvzeJLIU3oIn-QhOUu-e4",
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