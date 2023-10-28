<script lang="ts">
	import { BadgePlus } from 'lucide-svelte'

	export let title: string
	export let description: string | null | undefined = null
</script>

<a class="flex items-center rounded-2xl bg-blue-100 py-3 pl-5 pr-3 space-x-0.5" href="/">
	{#if !description}
		<span class="grow font-medium text-secondary-foreground truncate">{title}</span>
	{:else}
		<div class="flex grow flex-col -space-y-1 overflow-hidden">
			<span class="font-medium text-secondary-foreground truncate">{title}</span>
			<span class="text-xs text-muted-foreground truncate">{description}</span>
		</div>
	{/if}
	<span class="rounded-full bg-blue-200 p-3">
		<BadgePlus />
	</span>
</a>
