<script>
	import Icon from '@iconify/svelte';
	import { fade } from 'svelte/transition';

	const jobExperiences = [
		{
			year: 'since 2023',
			period: 'Aug. 2023–Present',
			company: 'Self-employed',
			position: 'Freelancing - DevOps Engineer',
			description:
				'Developing custom websites for clients. Providing expert consultation on IT server management, DevOps practices, and software development. Actively expanding skillset through personal projects, including managing Kubernetes clusters, web and native app development using various languages and frameworks.',
			current: true
		},
		{
			year: 'since 2023',
			period: 'Aug. 2023–Present',
			company: 'hoch.rein IT Solutions GmbH',
			position: 'Part-time DevOps Engineer',
			description:
				'Designing and implementing CI/CD pipelines using Jenkins and GitLab runners. Developing backend services with Node.js. Managing Linux servers for multiple web applications, ensuring high availability and performance.',
			current: true
		},
		{
			year: '2022',
			period: 'May 2022–July 2023',
			company: 'SmartStream Innovation Lab GmbH',
			position: 'DevOps Engineer',
			description:
				'Orchestrated DevOps practices for an AI-powered SaaS platform on AWS. Developed and optimized CI/CD pipelines using Jenkins, managed Kubernetes clusters with Helm and Ansible. Implemented comprehensive observability solutions using Prometheus and Grafana.',
			current: false
		},
		{
			year: '2015',
			period: 'Oct. 2015 - 2018',
			company: 'hoch.Rein IT-Solutions',
			position: 'IT-Specialist',
			description:
				'Managed Mobile-Device-Management solutions, administered storage systems, VMware servers, and databases. Handled firewall administration and provided customer support for national and international clients.',
			current: false
		}
	];

	const internships = [
		{
			year: '2020',
			period: 'Nov. 2020 - Feb. 2021',
			company: 'MindQ GmbH & Co. KG',
			position: 'Full-Stack Development Intern',
			description:
				'Developed a Progressive Web Application using VueJS and created microservices with Node.JS, Express, PostgreSQL, and MongoDB. Engaged in UI/UX design with Figma and AxureRP. Gained experience in DevOps practices, deploying applications in a Kubernetes cluster using Docker.',
			current: false
		}
	];

	let showMore = $state(false);

	let displayedJobs = $derived(showMore ? jobExperiences : jobExperiences.slice(0, 3));

	function toggleShowMore() {
		showMore = !showMore;
	}

	const iconName = $derived(showMore ? 'mdi:chevron-up' : 'mdi:chevron-down');
</script>

<section id="experience" class="bg-gray-900 px-4 py-16 text-gray-300">
	<div class="container mx-auto max-w-6xl px-4">
		<h2 class="mb-12 text-4xl font-bold tracking-wider text-white">Experience</h2>

		<div class="relative mb-12 text-center text-lg font-bold text-gray-300">
			<div class="inline-flex items-center">
				<div class="h-0.5 w-12 bg-pink-500"></div>
				<span class="mx-4 uppercase tracking-widest">JOBS</span>
				<div class="h-0.5 w-12 bg-pink-500"></div>
			</div>
		</div>
		<div class="relative mx-auto max-w-3xl">
			<div
				class="absolute left-0 top-0 h-full border-l-2 border-sky-500 md:left-0 md:border-l-2"
			></div>
			{#each displayedJobs as exp, index}
				<div class="mb-12 ml-6 md:ml-6 md:pl-10 md:text-left" transition:fade={{ duration: 100 }}>
					<span
						class="absolute -left-3 flex h-6 w-6 items-center justify-center rounded-full bg-purple-400 ring-8 ring-gray-900 md:left-0 md:-ml-3"
						class:glow={exp.current}
					>
						<span class="h-3 w-3 rounded-full bg-purple-600"></span>
					</span>
					<div>
						<p class="mb-1 text-sm font-semibold text-gray-500" class:text-purple-500={exp.current}>
							{exp.year}
						</p>
						<h3 class="mb-1 text-xl font-bold text-white">{exp.position}</h3>
						<p class="mb-2 text-lg text-gray-400">{exp.company}</p>
						<p class="mb-4 text-gray-400">{exp.period}</p>
						<p class="text-gray-400">{exp.description}</p>
					</div>
				</div>
			{/each}
		</div>

		{#if showMore}
			<div transition:fade={{ duration: 200 }}>
				<div class="relative mb-12 text-center text-lg font-bold text-gray-300">
					<div class="inline-flex items-center">
						<div class="h-0.5 w-12 bg-pink-500"></div>
						<span class="mx-4 uppercase tracking-widest">INTERNSHIPS</span>
						<div class="h-0.5 w-12 bg-pink-500"></div>
					</div>
				</div>
				<div class="relative mx-auto max-w-3xl">
					<div
						class="absolute left-0 top-0 h-full border-l-2 border-sky-500 md:left-0 md:border-l-2"
					></div>
					{#each internships as intern}
						<div
							class="mb-12 ml-6 md:ml-6 md:pl-10 md:text-left"
							transition:fade={{ duration: 350 }}
						>
							<span
								class="absolute -left-3 flex h-6 w-6 items-center justify-center rounded-full bg-purple-400 ring-8 ring-gray-900 md:left-0 md:-ml-3"
							>
								<span class="h-3 w-3 rounded-full bg-purple-600"></span>
							</span>
							<div>
								<p class="mb-1 text-sm font-semibold text-gray-500">{intern.year}</p>
								<h3 class="mb-1 text-xl font-bold text-white">{intern.position}</h3>
								<p class="mb-2 text-lg text-gray-400">{intern.company}</p>
								<p class="mb-4 text-gray-400">{intern.period}</p>
								<p class="text-gray-400">{intern.description}</p>
							</div>
						</div>
					{/each}
				</div>
			</div>
		{/if}
		<div class="flex justify-center">
			<button
				onclick={toggleShowMore}
				class="mx-auto flex flex-col items-center justify-center space-x-2 text-lg font-light"
			>
				<span>{showMore ? 'Show Less' : 'Show More'}</span>
				<Icon icon={iconName} width="20" height="20" />
			</button>
		</div>
	</div>
</section>

<style>
	@keyframes glow {
		0%,
		100% {
			box-shadow:
				0 0 5px #9f7aea,
				0 0 10px #9f7aea,
				0 0 15px rgb(196, 15, 232);
		}
		50% {
			box-shadow:
				0 0 10px #9f7aea,
				0 0 20px #9f7aea,
				0 0 30px rgb(196, 15, 232);
		}
	}

	.glow {
		animation: glow 1.5s ease-in-out infinite;
	}
</style>
