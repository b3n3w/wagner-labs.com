<script lang="ts">
	import Icon from '@iconify/svelte';
	import cloudMasterSwift from '$lib/assets/mockup-cloudmaster.png';
	import Tag from '../Tag.svelte';

	// Function to handle image error
	function handleImageError(event: Event): void {
		const target = event.target as HTMLImageElement;
		target.src = '/images/placeholder.png';
	}
</script>

<section id="projects" class="bg-gradient-to-b from-gray-900 to-gray-800 py-24 text-white">
	<div class="container mx-auto px-4">
		<h2 class="mb-20 text-center text-5xl font-bold">Projects</h2>

		<!-- CloudMaster Swift Project -->
		<div class="mb-32">
			<div class="grid grid-cols-1 items-center gap-8 lg:grid-cols-12">
				<!-- Left Column: Logo -->

				<!-- Middle Column: Title and Description -->
				<div class="flex flex-col text-left lg:col-span-5">
					<div class="mb-4 flex lg:col-span-2">
						<div class="h-16 w-16 rounded-2xl bg-purple-900 p-2">
							<img
								src="https://github.com/Ditectrev/CloudMaster-Swift/blob/main/Assets/CM_White.png?raw=true"
								alt="CloudMaster Swift Logo"
								class="h-full w-full object-contain"
								on:error={handleImageError}
							/>
						</div>
					</div>
					<h3 class="mb-6 text-4xl font-bold text-white">CloudMaster Swift</h3>
					<p class="mb-6 text-gray-300">
						CloudMaster Swift is a powerful iOS application designed to help users prepare for
						various cloud certification exams including AWS, Azure, GCP, Scrum, and more. The app
						offers different study modes including Training Mode and Exam Mode with varying
						difficulty levels.
					</p>
					<div class="mb-6 flex flex-wrap items-center gap-2">
						<Tag text="Swift" />
						<span
							class="rounded-full bg-purple-900 px-4 py-1 text-sm font-medium text-purple-200 transition-transform hover:-translate-y-1"
							>iOS</span
						>
						<span class="rounded-full bg-purple-900 px-4 py-1 text-sm font-medium text-purple-200"
							>Cloud</span
						>
						<a
							href="https://github.com/Ditectrev/CloudMaster-Swift"
							target="_blank"
							rel="noopener noreferrer"
							class="inline-flex items-center gap-2 self-start font-medium text-white transition-colors duration-150 hover:text-purple-400"
						>
							<Icon icon="mdi:github" width="24" height="24" />
						</a>
					</div>
				</div>

				<!-- Right Column: Screenshot with animation -->
				<div class="lg:col-span-5">
					<div class="relative">
						<img
							src={cloudMasterSwift}
							alt="CloudMaster Swift Screenshot"
							class="h-auto w-full transform rounded-xl transition-transform duration-700 hover:translate-y-[-10px]"
							on:error={handleImageError}
						/>
					</div>
				</div>
			</div>
		</div>

		<!-- Project B -->
		<div class="mb-32">
			<div class="grid grid-cols-1 items-center gap-8 lg:grid-cols-12">
				<!-- Left Column: Logo -->
				<div class="flex justify-center lg:col-span-2">
					<div class="h-28 w-28">
						<img
							src="/images/project-b.png"
							alt="Data Visualization Dashboard Logo"
							class="h-full w-full object-contain"
							on:error={handleImageError}
						/>
					</div>
				</div>

				<!-- Middle Column: Title and Description -->
				<div class="flex flex-col lg:col-span-5">
					<h3 class="mb-6 text-4xl font-bold text-purple-400">Data Visualization</h3>
					<p class="mb-6 text-gray-300">
						A comprehensive data visualization dashboard built with React and D3.js that transforms
						complex datasets into intuitive, interactive visualizations. The dashboard features
						real-time data updates, customizable charts, and responsive design for optimal viewing
						across devices.
					</p>
					<div class="mb-6 flex flex-wrap gap-2">
						<span class="rounded-full bg-purple-900 px-4 py-1 text-sm font-medium text-purple-200"
							>React</span
						>
						<span class="rounded-full bg-purple-900 px-4 py-1 text-sm font-medium text-purple-200"
							>D3.js</span
						>
						<span class="rounded-full bg-purple-900 px-4 py-1 text-sm font-medium text-purple-200"
							>TypeScript</span
						>
					</div>
					<a
						href="https://github.com/username/project-b"
						target="_blank"
						rel="noopener noreferrer"
						class="inline-flex items-center gap-2 self-start rounded-full bg-purple-600 px-6 py-2 font-medium text-white transition-all duration-300 hover:scale-105 hover:bg-purple-700"
					>
						<Icon icon="mdi:github" width="20" height="20" />
						<span>GitHub</span>
					</a>
				</div>

				<!-- Right Column: Screenshot with animation -->
				<div class="lg:col-span-5">
					<div class="relative">
						<img
							src="/images/project-b.png"
							alt="Data Visualization Dashboard Screenshot"
							class="h-auto w-full transform rounded-xl shadow-2xl transition-transform duration-700 hover:translate-y-[-10px]"
							on:error={handleImageError}
						/>
					</div>
				</div>
			</div>
		</div>

		<!-- Project C -->
		<div class="mb-32">
			<div class="grid grid-cols-1 items-center gap-8 lg:grid-cols-12">
				<!-- Left Column: Logo -->
				<div class="flex justify-center lg:col-span-2">
					<div class="h-28 w-28">
						<img
							src="/images/project-c.png"
							alt="Machine Learning API Logo"
							class="h-full w-full object-contain"
							on:error={handleImageError}
						/>
					</div>
				</div>

				<!-- Middle Column: Title and Description -->
				<div class="flex flex-col lg:col-span-5">
					<h3 class="mb-6 text-4xl font-bold text-purple-400">Machine Learning API</h3>
					<p class="mb-6 text-gray-300">
						A robust machine learning API service built with Python, Flask, and TensorFlow that
						provides pre-trained models for image recognition, natural language processing, and
						predictive analytics. The API includes comprehensive documentation, authentication, and
						rate limiting.
					</p>
					<div class="mb-6 flex flex-wrap gap-2">
						<span class="rounded-full bg-purple-900 px-4 py-1 text-sm font-medium text-purple-200"
							>Python</span
						>
						<span class="rounded-full bg-purple-900 px-4 py-1 text-sm font-medium text-purple-200"
							>Flask</span
						>
						<span class="rounded-full bg-purple-900 px-4 py-1 text-sm font-medium text-purple-200"
							>TensorFlow</span
						>
					</div>
					<a
						href="https://github.com/username/project-c"
						target="_blank"
						rel="noopener noreferrer"
						class="inline-flex items-center gap-2 self-start rounded-full bg-purple-600 px-6 py-2 font-medium text-white transition-all duration-300 hover:scale-105 hover:bg-purple-700"
					>
						<Icon icon="mdi:github" width="20" height="20" />
						<span>GitHub</span>
					</a>
				</div>

				<!-- Right Column: Screenshot with animation -->
				<div class="lg:col-span-5">
					<div class="relative">
						<img
							src="/images/project-c.png"
							alt="Machine Learning API Screenshot"
							class="h-auto w-full transform rounded-xl shadow-2xl transition-transform duration-700 hover:translate-y-[-10px]"
							on:error={handleImageError}
						/>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>
