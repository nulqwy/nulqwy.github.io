<script lang="ts">
	let { href, desc, icon }: { href: string; desc: string; icon: string | undefined } = $props();
</script>

<a {href} class="m-1">
	<div
		class="border-primary dark:border-primary-dark hover:border-accent hover:dark:border-accent-dark
					 hover:bg-secondary hover:dark:bg-secondary-dark active:bg-accent active:dark:bg-accent-dark bg-opacity-10
					 flex h-20 w-64 gap-2 rounded-md border
					 transition-colors hover:duration-0"
	>
		<div class="h-20 w-20 p-4">
			{#if icon}
				<img src={icon} alt="icon" class="text-color-filter h-full w-full" />
			{/if}
		</div>
		<div class="my-auto flex-auto">
			<p class="text-text dark:text-text-dark">{desc}</p>
		</div>
	</div>
</a>
