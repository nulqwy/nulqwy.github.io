<script lang="ts">
	// import type { Snippet } from 'svelte';

	let { children }: { children: any } = $props();
</script>

<h1
	class="text-text dark:text-text-dark major-mono-display-regular stripe-background-accent text-8xl"
>
	{@render children()}
</h1>
