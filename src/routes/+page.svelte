<script>
	import { mdiLinkedin, mdiGithub } from '@mdi/js';
	import logo from '$lib/assets/logo.png';
</script>

<main>
	<div class="container">
		<div class="row text-center">
			<div class="col-12">
				<h1 class="text-h4 font-weight-thin">Build in progress</h1>
				<img alt="Wagner-Lab Logo" src={logo} />
				<p class="font-weight-thin">BENEDIKT WAGNER</p>
			</div>
			<div class="col">
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

<style>
	.container {
		height: 100vh;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.row {
		width: 100%;
	}
	.text-center {
		text-align: center;
	}
	.text-h4 {
		font-size: 2.125rem;
	}
	.font-weight-thin {
		font-weight: 100;
	}
	.my-3 {
		margin-top: 1rem;
		margin-bottom: 1rem;
	}
	img {
		max-height: 200px;
		width: auto;
	}
	.btn-icon {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		padding: 0.5rem;
		margin: 0 0.25rem;
		color: inherit;
		text-decoration: none;
	}
</style>
