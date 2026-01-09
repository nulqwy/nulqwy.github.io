<script lang="ts">
	// import type { Snippet } from 'svelte';

	let { children }: { children: any } = $props();
</script>

<h2
	class="text-text dark:text-text-dark major-mono-display-regular stripe-background mt-14 text-7xl"
>
	{@render children()}
</h2>
