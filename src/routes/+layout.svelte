<script lang="ts">
	import '../app.css';
	import Analytics from '$lib/analytics.svelte';
	import Footer from './footer.svelte';
	import Navbar from './navbar.svelte';
	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<Analytics />
<Navbar />
{@render children?.()}
<Footer />
