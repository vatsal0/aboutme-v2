<template>
<div>
	<v-container fluid style="min-height:100vh">
		<v-row justify="center" width="100%">
			<v-col cols="12" sm="8">
				<v-card>
					<h1 class="py-4 text-wrap text-center">{{title}}</h1>
					<v-card-title class="headline d-flex flex-column justify-center">
						<v-avatar size="16rem" class="mx-auto mb-4">
							<img src="headshot.jpeg">
						</v-avatar>
						Welcome to my page!
					</v-card-title>

					<v-card-text class="text-center">
						<p>I'm an undergraduate computer science student interested in machine learning and finance. Currently, I am a freshman at the University of Maryland. You can view my resume <a
								href="resume.pdf"
								target="_blank"
							>here</a>.</p>
						
						<p>
							Click on the links on the sidebar to learn more about me!
						</p>

						<hr class="my-3">
					</v-card-text>
					<v-card-actions>
						<div class="d-flex flex-column flex-lg-row justify-space-around align-center flex-grow-1">
							<v-btn 
								:href="link.to"
								target="_blank"
								v-for="(link, i) in links"
								:key="i"
								class="my-2 my-lg-auto d-flex"
							>
								<v-icon>{{link.icon}}</v-icon>
								<p
									class="ml-2 my-auto text-caption"
								>{{link.title}}</p>
							</v-btn>
						</div>
							
					</v-card-actions>
				</v-card>
			</v-col>
		</v-row>
	</v-container>

	<v-container fluid style="min-height:100vh" id="experience">
		<h1 class="text-center">Experience</h1>
	</v-container>

	<v-container fluid style="min-height:100vh" id="education">
		<h1 class="text-center">Education</h1>
	</v-container>

	<v-container fluid style="min-height:100vh" id="projects">
		<h1 class="text-center">Projects</h1>
	</v-container>
</div>
</template>

<script>
export default {
	data () {
    return {
      links: [
        {
          icon: 'mdi-email',
          title: 'Send me an email',
          to: 'mailto:vatsalbaherwani@gmail.com'
        },
        {
          icon: 'mdi-linkedin',
          title: 'Connect with me on linkedin',
          to: 'https://www.linkedin.com/in/vatsal-baherwani'
        },
        {
          icon: 'mdi-github',
          title: 'View my projects on GitHub',
          to: 'https://www.github.com/vatsal0'
        }
      ],
      miniVariant: false,
      title: 'Vatsal Baherwani'
    }
  }
}
</script>