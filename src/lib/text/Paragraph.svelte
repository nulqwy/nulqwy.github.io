<script lang="ts">
	// import type { Snippet } from 'svelte';
	import Header from './Header.svelte';
	import Text from './Text.svelte';

	let { name, children }: { name: string; children: any } = $props();
</script>

<section>
	<div class="w-full">
		<Header>{name}</Header>
	</div>

	<Text>{@render children()}</Text>
</section>
