<script lang="ts">
	// import type { Snippet } from 'svelte';

	let { children }: { children?: any } = $props();
</script>

{#if children}
	<div class="mt-8 inline-flex w-full items-center justify-center">
		<hr
			class="border-secondary dark:border-secondary-dark bg-secondary dark:bg-secondary-dark my-4 h-0.5 w-full rounded border"
		/>
		<div
			class="bg-background dark:bg-background-dark absolute left-1/2 -translate-x-1/2 px-3 font-medium"
		>
			{@render children()}
		</div>
	</div>
{:else}
	<hr class="bg-primary dark:bg-primary-dark my-20 h-1 rounded border" />
{/if}
