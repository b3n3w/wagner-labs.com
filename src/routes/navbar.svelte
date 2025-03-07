<script>
	import logo from '$lib/assets/logo.png';
</script>

<nav class="w-full px-4 py-2 md:px-16">
	<div class="container mx-auto flex flex-col items-center justify-between md:flex-row">
		<a href="/" class="mb-4 md:mb-0">
			<img src={logo} alt="Logo" class="h-12 md:h-14" />
		</a>
		<div class="space-x-4 text-white">
			<a href="/#about" class="transition-colors duration-300 hover:text-purple-500">About Me</a>
			<a href="/#skills" class="transition-colors duration-300 hover:text-purple-500">Skills</a>
			<a href="/#projects" class="transition-colors duration-300 hover:text-purple-500">Projects</a>
			<a href="/#contact" class="transition-colors duration-300 hover:text-purple-500">Contact</a>
		</div>
	</div>
</nav>
