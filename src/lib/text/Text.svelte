<script lang="ts">
	// import type { Snippet } from 'svelte';

	let { children }: { children: any } = $props();
</script>

<p class="text-text dark:text-text-dark">
	{@render children()}
</p>
