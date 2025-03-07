<script lang="ts">
	import '../app.css';
	import Footer from './footer.svelte';
	import Navbar from './navbar.svelte';
	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<Navbar />
{@render children?.()}
<Footer />
