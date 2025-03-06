<script>
	import HeroSection from '$lib/components/SectionHero.svelte';
	import AboutSection from '$lib/components/SectionAbout.svelte';
	import SkillSection from '$lib/components/SectionSkills.svelte';
	import ExperienceSection from '$lib/components/SectionExperience.svelte';
	import ContactSection from '$lib/components/SectionContact.svelte';
</script>
<svelte:head>
	<title>Benedikt Wagner | DevOps Engineer</title>
	<meta name="description" content="Personal portfolio showcasing skills, experience, and projects in web development." />
	<meta name="keywords" content="web developer, portfolio, skills, experience, projects" />
	
	<!-- Open Graph / Social Media -->
	<meta property="og:title" content="Benedikt Wagner | DevOps Engineer" />
	<meta property="og:description" content="Personal portfolio showcasing skills, experience, and projects." />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://www.wagner-labs.com" />

	<!-- Twitter Card -->
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="Benedikt Wagner | DevOps Engineer" />
	<meta name="twitter:description" content="Personal portfolio showcasing skills, experience, and projects." />
	
	<!-- Canonical URL -->
	<link rel="canonical" href="https://www.wagner-labs.com" />
</svelte:head>
<div class="min-h-screen">
	<main class=" w-full">
		<HeroSection />

		<AboutSection />

		<SkillSection />

		<ExperienceSection />

		<ContactSection />
	</main>
</div>
