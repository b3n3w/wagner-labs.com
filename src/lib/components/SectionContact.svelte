<script lang="ts">
	import { mdiEmail, mdiMapMarker } from '@mdi/js';
	import { mdiLinkedin, mdiGithub } from '@mdi/js';
</script>

<section id="contact" class="w-full bg-gray-800 py-16 text-white">
	<div class="container mx-auto max-w-6xl px-4">
		<h2 class="relative mb-12 text-center text-4xl font-bold">
			<span class="relative z-10 bg-gray-800 px-4 tracking-wider">Contact Me</span>
			<div class="-z-1 absolute left-0 top-1/2 h-0.5 w-full bg-purple-500"></div>
		</h2>

		<div
			class="mb-12 flex flex-col items-center justify-center space-y-4 md:flex-row md:space-x-4 md:space-y-0"
		>
			<a
				href="mailto:benedikt@wagner-labs.com"
				class="flex items-center rounded-lg bg-gray-700 p-4 md:w-auto"
			>
				<svg class="mr-3 h-6 w-6 text-white" viewBox="0 0 24 24">
					<path fill="currentColor" d={mdiEmail} />
				</svg>
				<span>benedikt@wagner-labs.com</span>
			</a>
			<div class="flex items-center rounded-lg bg-gray-700 p-4">
				<svg class="mr-3 h-6 w-6" viewBox="0 0 24 24">
					<path fill="currentColor" d={mdiMapMarker} />
				</svg>
				<span>Würzburg, Bavaria, Germany</span>
			</div>
		</div>

		<div class="flex justify-center space-x-6">
			<a
				href="https://www.linkedin.com/in/benedikt-wagner-808a101a9/"
				class=" transition-colors duration-300 hover:text-purple-500"
			>
				<svg class="h-8 w-8" viewBox="0 0 24 24">
					<path fill="currentColor" d={mdiLinkedin} />
				</svg>
			</a>
			<a
				href="https://github.com/b3n3w"
				class=" transition-colors duration-300 hover:text-purple-500"
			>
				<svg class="h-8 w-8" viewBox="0 0 24 24">
					<path fill="currentColor" d={mdiGithub} />
				</svg>
			</a>
		</div>
	</div>
</section>
