<script lang="ts">
	// import type { Snippet } from 'svelte';

	let { children }: { children: any } = $props();
</script>

<h1
	class="old-standard-tt-bold major-mono-display-regular stripe-background-accent text-8xl text-text dark:text-text-dark"
>
	{@render children()}
</h1>
