<script>
	import { mdiLinkedin, mdiGithub } from '@mdi/js';
	import logo from '$lib/assets/logo.png';
</script>

<main>
	<div class="flex justify-center text-center items-center">
		<div class="flex flex-col">
			<div class="flex flex-col gap-5">
				<h1 class="text-3xl uppercase font-light">Build in progress</h1>
				<img alt="Wagner-Lab Logo" src={logo} />
				<p class="text-xl font-thin">BENEDIKT WAGNER</p>
			</div>
			<div class="flex flex-row justify-center mt-4">
				<a href="https://www.linkedin.com/in/benedikt-wagner-808a101a9/" class="btn btn-icon">
					<svg viewBox="0 0 24 24" width="36" height="36">
						<path fill="currentColor" d={mdiLinkedin} />
					</svg>
				</a>
				<a
					href="https://github.com/b3n3w"
					target="_blank"
					rel="noopener noreferrer"
					class="btn btn-icon"
				>
					<svg viewBox="0 0 24 24" width="36" height="36">
						<path fill="currentColor" d={mdiGithub} />
					</svg>
				</a>
			</div>
		</div>
	</div>
</main>
