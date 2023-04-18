<template>
	<v-container fluid style="min-height:100vh; width: 100%" id="experience">
		<h1 class="text-center">Experience</h1>

		<div>
			<v-timeline :dense="$vuetify.breakpoint.mdAndDown">
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
          time: "Feb 2023 - Present",
          title: "Research Assistant",
          place: "University of Maryland",
          desc: ["Working with Dr. Serhiy Kozak and Dr. Shri Santosh on a machine learning options pricing model",
            "Inferring Black-Scholes implied volatility of at-the-money call options with linear interpolation",
            "Fitting implied vol as a function of expected return with post-lasso OLS regression on Laguerre polynomials"],
          img: "https://media.licdn.com/dms/image/C560BAQHrhLnmmZTGjQ/company-logo_100_100/0/1519856141972?e=1689811200&v=beta&t=qRxRYxW3xkXjjt7yrsHYqCrR-jS8Fd8jPFdXa9eRS0k",
        },
        {
          time: "Sep 2022 - Dec 2022",
          title: "Research Assistant",
          place: "University of Maryland",
          desc: ["Worked with Dr. Alec Solway at the Computational Cognitive Neuroscience & Psychiatry Lab",
            "Developed machine learning classifiers to analyze electroencephalography data and study the process of human decision making",
            "Achieved 80% accuracy in predicting patient response from EEG data with a convolutional neural network"],
            img: "https://media.licdn.com/dms/image/C560BAQHrhLnmmZTGjQ/company-logo_100_100/0/1519856141972?e=1689811200&v=beta&t=qRxRYxW3xkXjjt7yrsHYqCrR-jS8Fd8jPFdXa9eRS0k",
        },
        {
          time: "May 2022 - Aug 2022",
          title: "Software Engineer Intern",
          place: "Bloomberg LP",
          desc: ["Designed workflow in Apache Airflow to optimize calculation of 72 indicators for >3 million fixed-income securities at market close",
            "Parallelized execution workload across 5 remote Linux host machines",
            "Reduced market snapshot calculation runtime by 35%",
            "Implemented dynamic error handling and recalculation workflow to minimize failure rate"],
          img: "https://media.licdn.com/dms/image/C4D0BAQF0uyE7RGKDGg/company-logo_100_100/0/1531146047122?e=1689811200&v=beta&t=UmRJ4r7O6dXTWTcXogT1JbEdjBX4qaArdcewsZinFOA",
        },
        {
          time: "Feb 2022 - Dec 2022",
          title: "Investment Analyst",
          place: "TAMID Group @ UMD",
          desc: ["Conducted market research and analysis on TAMID's ~$10,000 investment portfolio",
            "Curated 3 stock pitches for potential new investments"],
          img: "https://media.licdn.com/dms/image/C560BAQHQaYiTbnfxaw/company-logo_200_200/0/1656828321908?e=2147483647&v=beta&t=IRSDFindouuSvQadaOFGbONwE5D4f0NS2lWrntxH034",
        },
        {
          time: "Jan 2022 - Dec 2022",
          title: "Content Team Lead",
          place: "International Economics and Finance Society @ UMD",
          desc: ["Prepared educational presentations on economics and finance topics for 200+ club members"],
          img: "https://media.licdn.com/dms/image/C560BAQHCCUZeb_eMHA/company-logo_100_100/0/1519904563700?e=1689811200&v=beta&t=ZSeOMXn9JxCfdxWIQO9VDwAKE7BDcVGrUf3Qt9kxLPY",
        },
        {
          time: "Jan 2022 - May 2022",
          title: "Software Engineer Intern",
          place: "Capital One",
          desc: ["Developed React dashboard to monitor transcripts for ~7 million calls/wk",
            "Deployed Docker images of sentiment analysis and classification models",
            "Visualized data with Python Dash to display insights on call center trends and customer satisfaction"],
          img: "https://media.licdn.com/dms/image/C560BAQF0OgQyRZ9yAA/company-logo_100_100/0/1635782717682?e=1689811200&v=beta&t=R-mDeUj505i5IRhK3ZxW4Hi_CwcD2rH-Xp5I9SWNQpU",
        },
        {
          time: "Dec 2021 - May 2022",
          title: "Research Assistant",
          place: "University of Maryland",
          desc: ["Worked with Dr. Lars Olson in the Department of Agriculture and Resource Economics",
            "Wrote a web scraper to collect invasive species data from the CABI Invasive Species Compendium",
            "Developed NLP model to infer economic impact of invasive species and classify prominent threats",
            "Achieved >90% accuracy in detecting phrases related to economic impact"],
          img: "https://media.licdn.com/dms/image/C560BAQHrhLnmmZTGjQ/company-logo_100_100/0/1519856141972?e=1689811200&v=beta&t=qRxRYxW3xkXjjt7yrsHYqCrR-jS8Fd8jPFdXa9eRS0k",
        },
        {
          time: "Nov 2021 - May 2022",
          title: "Technical Lead",
          place: "Google Developer Student Club @ UMD",
          desc: ["Organized educational workshops teaching Google Cloud, Android, and Firebase"],
          img: "https://media.licdn.com/dms/image/C4E0BAQE_1tNZKj3sNQ/company-logo_100_100/0/1617607397103?e=1689811200&v=beta&t=uOHN_IeYQauhK3TnwnIYhAThpVCNJzmdIF91Z9QDyn0",
        },
        {
          time: "Oct 2021 - May 2022",
          title: "Vice President",
          place: "Student Life Council @ UMD",
          desc: ["Managed $7,000 budget to plan events for over 1,000 students in the University Honors program",
            "Coordinated with 10 other council members to handle  logistics and increase student involvement"],
            img: "https://media.licdn.com/dms/image/C560BAQHrhLnmmZTGjQ/company-logo_100_100/0/1519856141972?e=1689811200&v=beta&t=qRxRYxW3xkXjjt7yrsHYqCrR-jS8Fd8jPFdXa9eRS0k",
        },
        {
          time: "Sep 2020 - Aug 2021 ",
          title: "Software Engineer Intern",
          place: "Bloomberg LP",
          desc: ["Developed Java Spring REST API to create, read, update, and delete Bloomberg Law permissions",
            "Designed Rails + Vue.js dashboard to provide analytics on permission usage",
            "Reduced Bloomberg Law login time by >200ms through removing 300+ deprecated permissions"],
          img: "https://media.licdn.com/dms/image/C4D0BAQF0uyE7RGKDGg/company-logo_100_100/0/1531146047122?e=1689811200&v=beta&t=UmRJ4r7O6dXTWTcXogT1JbEdjBX4qaArdcewsZinFOA",
        },
			]
		}
	}
}
</script>