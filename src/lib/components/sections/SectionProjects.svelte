<script lang="ts">
	import Icon from '@iconify/svelte';
	import cloudMasterSwift from '$lib/assets/mockup-cloudmaster.png';
	import soulEventsToday from '$lib/assets/mockup-soul-events.png';
	import logoSoulEventsToday from '$lib/assets/logo-soul-events.png';
	import Tag from '../Tag.svelte';
	import { goto } from '$app/navigation';

	// Function to handle image error
	function handleImageError(event: Event): void {
		const target = event.target as HTMLImageElement;
		target.src = '/images/placeholder.png';
	}
</script>

<section id="projects" class="pb-24 pt-10 text-white">
	<div class="container mx-auto px-4">
		<h2 class="mb-12 text-4xl font-bold tracking-wider text-white">Projects</h2>
		<!-- CloudMaster Swift Project -->
		<div class="mb-32 flex">
			<div class="grid grid-cols-1 items-center gap-8 lg:grid-cols-12">
				<!-- Left Column: Logo -->

				<!-- Middle Column: Title and Description -->
				<div class="flex flex-col sm:text-center md:text-left lg:col-span-5">
					<div class="mb-4 flex justify-center md:justify-start lg:col-span-2">
						<div class="h-16 w-16 rounded-2xl p-2">
							<img
								src="https://github.com/Ditectrev/CloudMaster-Swift/blob/main/Assets/CM_White.png?raw=true"
								alt="CloudMaster Swift Logo"
								class="h-full w-full object-contain"
								onerror={handleImageError}
							/>
						</div>
					</div>
					<h3 class="mb-6 font-mono text-2xl font-bold uppercase tracking-wider text-white">
						CloudMaster
					</h3>
					<p class="mb-6 text-gray-300">
						CloudMaster Swift is native Swift application designed to help users prepare for various
						cloud certification exams including AWS, Azure, GCP, Scrum, and more. This app was
						developed as a experiment to learn Swift and SwiftUI.
					</p>
					<div class="mb-6 flex flex-wrap items-center justify-center gap-2 md:justify-start">
						<Tag text="Swift" />
						<Tag text="iOS" />
						<Tag text="Cloud" />
					</div>
					<div class="flex justify-center gap-4 md:justify-start">
						<button
							onclick={() =>
								window.open('https://github.com/Ditectrev/CloudMaster-Swift', '_blank')}
							class="inline-flex items-center text-white transition-all duration-200 hover:translate-y-[-2px] hover:text-purple-700"
						>
							<Icon icon="mdi:github" width="40" height="40" />
						</button>
						<button
							onclick={() =>
								window.open(
									'https://apps.apple.com/de/app/cloudmaster-swift/id6503601139?l=en-GB',
									'_blank'
								)}
							class="inline-flex items-center text-white transition-all duration-200 hover:translate-y-[-2px] hover:text-purple-700"
						>
							<Icon icon="mingcute:appstore-fill" width="40" height="40" />
						</button>
					</div>
				</div>

				<!-- Right Column: Screenshot with animation -->
				<div class="lg:col-span-5">
					<div class="relative">
						<img
							src={cloudMasterSwift}
							alt="CloudMaster Swift Screenshot"
							class="h-auto w-full transform rounded-xl transition-transform duration-700 hover:translate-y-[-10px]"
							onerror={handleImageError}
						/>
					</div>
				</div>
			</div>
		</div>

		<!-- Soul-Events Today Project -->
		<div class="mb-32 flex">
			<div class="grid grid-cols-1 items-center gap-8 lg:grid-cols-12">
				<!-- Left Column: Screenshot with animation (moved to left for larger screens) -->
				<div class="order-2 lg:order-1 lg:col-span-6">
					<div class="relative">
						<img
							src={soulEventsToday}
							alt="Soul-Events Today Screenshot"
							class="h-auto w-full transform rounded-xl transition-transform duration-700 hover:translate-y-[-10px]"
							onerror={handleImageError}
						/>
					</div>
				</div>

				<!-- Right Column: Title and Description (moved to right for larger screens) -->
				<div
					class="order-1 flex flex-col sm:text-center lg:order-2 lg:col-span-6 lg:pl-8 lg:text-right"
				>
					<div class="mb-4 flex justify-center md:justify-start lg:justify-end">
						<div class="h-16 w-16 rounded-2xl p-2">
							<img
								src={logoSoulEventsToday}
								alt="Soul-Events Today Logo"
								class="h-full w-full object-contain"
								onerror={handleImageError}
							/>
						</div>
					</div>
					<h3 class="mb-6 font-mono text-2xl font-bold uppercase tracking-wider text-white">
						Soul-Events Today
					</h3>
					<p class="mb-6 text-gray-300">
						Soul-Events Today is a modern web application for discovering and managing concious
						events. The platform allows users to create events, manage their events, and connect
						with other users.
					</p>
					<div
						class="mb-6 flex flex-wrap items-center justify-center gap-2 md:justify-start lg:justify-end"
					>
						<Tag text="Webdevelopment" />
						<Tag text="SvelteKit" />
						<Tag text="Supabase" />
					</div>
					<div class="flex justify-center gap-4 md:justify-start lg:justify-end">
						<button disabled class="inline-flex items-center text-white">
							<div class="flex flex-col items-center gap-1 text-center">
								<Icon
									class="duration-200 hover:text-gray-400"
									icon="mdi:github"
									width="40"
									height="40"
								/>
								<span class="text-sm text-gray-400">Not available yet</span>
							</div>
						</button>
						<button
							onclick={() => window.open('https://soul-events.today', '_blank')}
							class="inline-flex items-center text-white"
						>
							<div class="flex flex-col items-center gap-1 text-center">
								<Icon
									class="transition-all duration-200 hover:translate-y-[-2px] hover:text-purple-700"
									icon="mdi:web"
									width="40"
									height="40"
								/>
								<span class="text-sm text-gray-400">Website</span>
							</div>
						</button>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>
