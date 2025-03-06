<script lang="ts">
	import portrait from '$lib/assets/portrait.png';
</script>

<section id="hero" class="px-4 py-16 md:px-8 lg:px-16">
	<div class="container mx-auto max-w-6xl">
		<div class="flex flex-col items-center md:flex-row md:justify-between">
			<div class="mb-8 text-center md:mb-0 md:w-1/2 md:text-left">
				<h1 class="mb-4 text-4xl font-bold md:text-5xl lg:text-6xl">Benedikt Wagner</h1>
				<h2 class="mb-4 text-xl font-semibold md:text-2xl">
					Something in between DevOps and your typical nerd
				</h2>
				<button
					class="rounded-full bg-[rgb(49,9,100)] px-6 py-2 text-white transition-colors duration-300 hover:bg-gradient-to-r hover:from-purple-600 hover:to-pink-800"
					onclick={() => document.getElementById('contact').scrollIntoView({ behavior: 'smooth' })}
				>
					Contact Me
				</button>
			</div>

			<div class="flex w-full justify-center md:w-1/2 md:justify-end">
				<div class="relative h-80 w-64 overflow-hidden md:h-96 md:w-80">
					<img
						class="absolute inset-0 h-full w-full object-cover"
						src={portrait}
						alt="Benedikt Wagner"
					/>
					<div
						class="absolute inset-0"
						style="
				 background-image:
				   linear-gradient(to right, #0f0f1a 0%, transparent 20%, transparent 80%, #0f0f1a 100%),
				   linear-gradient(to bottom, #0f0f1a 0%, transparent 20%, transparent 80%, #0f0f1a 100%),
				   radial-gradient(circle at top left, #0f0f1a 0%, transparent 30%),
				   radial-gradient(circle at top right, #0f0f1a 0%, transparent 30%),
				   radial-gradient(circle at bottom left, #0f0f1a 0%, transparent 30%),
				   radial-gradient(circle at bottom right, #0f0f1a 0%, transparent 30%);
			   "
					></div>
				</div>
			</div>
		</div>
	</div>
</section>
