<script lang="ts">
	import type { SvelteComponent } from 'svelte';

	interface Props {
		skillName: string;
		skillURL: string;
		skillIcon: typeof SvelteComponent;
	}

	let { skillName, skillURL, skillIcon }: Props = $props();

	const SvelteComponent_1 = $derived(skillIcon);
</script>

<a href={skillURL}>
	<div
		class="flex cursor-pointer flex-col items-center rounded-lg bg-gray-800 p-2 text-center shadow-md transition-all duration-300 hover:bg-purple-900 hover:text-purple-200
           hover:shadow-lg hover:shadow-purple-500/50"
	>
		<SvelteComponent_1 size={30} />
		<p class="mt-2 text-xs">{skillName}</p>
	</div>
</a>
