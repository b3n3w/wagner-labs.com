<script lang="ts">
	import '../app.css';
	import Analytics from '$lib/analytics.svelte';
	import Footer from './footer.svelte';
	import Navbar from './navbar.svelte';
</script>

<Analytics />
<Navbar />
<slot />
<Footer />
