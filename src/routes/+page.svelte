<script>
	import AnimatedHeader from './AnimatedHeader.svelte';

	let loaded = false;
</script>

<button
	on:click={() => {
		loaded = true;
	}}>loaded</button
>

<AnimatedHeader title="Product" visible={loaded} />
