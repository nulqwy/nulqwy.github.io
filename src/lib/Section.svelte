<script lang="ts">
	// import type { Snippet } from 'svelte';
	import LineBreak from './decorations/LineBreak.svelte';
	import Text from './text/Text.svelte';

	let {
		children,
		name,
		separator = true,
		flex = false
	}: { children: any; name: string; separator?: boolean; flex?: boolean } = $props();
</script>

<section id={name} class="lg:mx-auto lg:max-w-5xl">
	{#if separator}
		<LineBreak><Text>{name}</Text></LineBreak>
	{/if}

	{#if flex}
		<div class="flex flex-wrap justify-center">
			{@render children()}
		</div>
	{:else}
		{@render children()}
	{/if}
</section>
