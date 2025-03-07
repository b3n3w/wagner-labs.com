<script>
	import { ChevronDown, ChevronUp } from 'lucide-svelte';
	import { slide, fade } from 'svelte/transition';
	import Skill from '$lib/components/Skill.svelte';

	// infrastructure
	import IconAWS from '$lib/icons/infrastructure/IconAWS.svelte';
	import IconK8s from '$lib/icons/infrastructure/IconK8s.svelte';
	import IconLinux from '$lib/icons/infrastructure/IconLinux.svelte';
	import IconProxmox from '$lib/icons/infrastructure/IconProxmox.svelte';
	// languages
	import IconJava from '$lib/icons/languages/IconJava.svelte';
	import IconGolang from '$lib/icons/languages/IconGolang.svelte';
	import IconPython from '$lib/icons/languages/IconPython.svelte';
	import IconTypeScript from '$lib/icons/languages/IconTypeScript.svelte';
	import IconSwift from '$lib/icons//languages/IconSwift.svelte';
	// databases
	import IconMongo from '$lib/icons/databases/IconMongo.svelte';
	import IconPostgres from '$lib/icons/databases/IconPostgres.svelte';
	import IconRedis from '$lib/icons/databases/IconRedis.svelte';
	// tools
	import IconAnsible from '$lib/icons/tools/IconAnsible.svelte';
	import IconHelm from '$lib/icons/tools/IconHelm.svelte';
	import IconFigma from '$lib/icons/tools/IconFigma.svelte';

	let showMore = $state(false);

	const skills = {
		languages: [
			{ name: 'TypeScript', icon: IconTypeScript, url: 'https://www.typescriptlang.org/' },
			{ name: 'Python', icon: IconPython, url: 'https://www.python.org/' },
			{ name: 'Golang', icon: IconGolang, url: 'https://golang.org/' },
			{ name: 'Java', icon: IconJava, url: 'https://www.java.com/' },
			{ name: 'Swift', icon: IconSwift, url: 'https://swift.org/' }
		],
		infrastructure: [
			{ name: 'Kubernetes', icon: IconK8s, url: 'https://kubernetes.io/' },
			{ name: 'AWS', icon: IconAWS, url: 'https://www.docker.com/' },
			{ name: 'Linux', icon: IconLinux, url: 'https://www.linux.org/' },
			{ name: 'Proxmox', icon: IconProxmox, url: 'https://www.proxmox.com/' }
		],
		databases: [
			{ name: 'MongoDB', icon: IconMongo, url: 'https://www.mongodb.com/' },
			{ name: 'PostgreSQL', icon: IconPostgres, url: 'https://www.postgresql.org/' },
			{ name: 'Redis', icon: IconRedis, url: 'https://redis.io/' }
		],
		tools: [
			{ name: 'Helm', icon: IconHelm, url: 'https://helm.sh/' },
			{ name: 'Ansible', icon: IconAnsible, url: 'https://www.ansible.com/' },
			{ name: 'Figma', icon: IconFigma, url: 'https://www.figma.com/' }
		]
	};

	function toggleShowMore() {
		showMore = !showMore;
	}

	const SvelteComponent = $derived(showMore ? ChevronUp : ChevronDown);
</script>

<section id="skills" class="justify-center px-8 py-16 text-center md:px-16">
	<div class="container mx-auto max-w-6xl px-4">
		<h2 class="mb-8 text-3xl font-bold tracking-wider">My Skills</h2>

		<section id="infrastructure" class="mb-4">
			<h3 class="mb-4 text-center text-2xl font-bold">Infrastructure</h3>
			<div class="grid grid-cols-4 gap-2 md:grid-cols-3 lg:grid-cols-5">
				{#each skills.infrastructure as skill}
					<Skill skillURL={skill.url} skillName={skill.name} skillIcon={skill.icon} />
				{/each}
			</div>
		</section>

		{#if showMore}
			<div class="mb-8" transition:slide={{ duration: 300 }}>
				<section id="languages" class="mb-4" transition:fade={{ duration: 200 }}>
					<h3 class="mb-4 text-center text-2xl font-bold">Coding</h3>
					<div class=" grid grid-cols-4 gap-2 md:grid-cols-3 lg:grid-cols-5">
						{#each skills.languages as skill}
							<Skill skillName={skill.name} skillURL={skill.url} skillIcon={skill.icon} />
						{/each}
					</div>
				</section>

				<section id="databases" class="mb-4" transition:fade={{ duration: 200, delay: 50 }}>
					<h3 class="mb-4 text-center text-2xl font-bold">Databases</h3>
					<div class="grid grid-cols-4 gap-2 md:grid-cols-4 lg:grid-cols-5">
						{#each skills.databases as skill}
							<Skill skillName={skill.name} skillURL={skill.url} skillIcon={skill.icon} />
						{/each}
					</div>
				</section>

				<section id="tools" transition:fade={{ duration: 200, delay: 100 }}>
					<h3 class="mb-4 text-center text-2xl font-bold">Tools</h3>
					<div class="grid grid-cols-4 gap-2 md:grid-cols-4 lg:grid-cols-5">
						{#each skills.tools as skill}
							<Skill skillName={skill.name} skillURL={skill.url} skillIcon={skill.icon} />
						{/each}
					</div>
				</section>
			</div>
		{/if}

		<button
			onclick={toggleShowMore}
			class="mx-auto flex flex-col items-center justify-center space-x-2 text-lg font-light"
		>
			<span>{showMore ? 'Show Less' : 'Show More'}</span>
			<SvelteComponent size={20} />
		</button>
	</div>
</section>
