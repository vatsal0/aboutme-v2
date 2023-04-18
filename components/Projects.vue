<template>
	<v-container fluid style="min-height:100vh; width: 100%" id="projects">
		<h1 class="text-center">Projects</h1>

		<div class="d-flex flex-md-row flex-column flex-wrap justify-center">
			<v-card
				v-for="(item, i) in items"
				:key="i"
				dark
				class="my-4 py-4 d-flex flex-column justify-space-between mx-md-4 mx-8"
				:width="$vuetify.breakpoint.mdAndDown ? '100%' : '20rem'"
			>
				<div class="text-md-left text-center px-4">
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
						color="accent"
						text
						class="mx-md-2 mx-auto"
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
					title: "MNIST Digit Classifier",
					desc: "Deep neural network written from scratch in C implementing batch gradient descent and regularization. Achieved a 97.1% test set accuracy in classifying the MNIST image database of 10,000 handwritten digits.",
					source: "https://github.com/vatsal0/mnist-digit-classifier",
				},
			]
		}
	}
}
</script>
