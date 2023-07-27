<script lang="ts">
	import { fade } from 'svelte/transition';

	export let title = 'Title';
	export let visible = true;
</script>

<section>
	{#if visible}
		<h1>
			{#each title as l, i}
				<span in:fade|global={{ delay: 600 + i * 100, duration: 700 }}>{l}</span>
			{/each}
		</h1>
		<a href="./store" in:fade|global={{ delay: title.length * 100 + 1200 }}>order now!</a>
	{/if}
</section>

<svelte:head>
	<link
		href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;700&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<style>
	section {
		font-family: 'IBM Plex Mono', monospace;
	}
	h1 {
		font-weight: 700;
		font-size: max(8vw, 3rem);
		margin-bottom: 1rem;
	}
	a {
		font-weight: 700;
		font-size: 2.5rem;
	}
	section {
		padding: 5rem 5rem 5rem 7rem;
	}
</style>
