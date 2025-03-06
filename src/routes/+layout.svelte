<script lang="ts">
	import '../app.css';
	import Footer from './footer.svelte';
	import Navbar from './navbar.svelte';
</script>

<Navbar />
<slot />
<Footer />
