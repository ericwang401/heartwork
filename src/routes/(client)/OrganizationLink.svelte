<script lang="ts">
	import { cn, stringToTailwindColor } from '$lib/utils'
	import { BadgePlus } from 'lucide-svelte'

	export let title: string
	export let description: string | null | undefined = null

	$: background = `bg-${stringToTailwindColor(title)}-100`
	$: accent = `bg-${stringToTailwindColor(title)}-200`
</script>

<a class={cn(' space-x-0.5 rounded-2xl py-6 pl-5 pr-3', background)} href="/">
	{#if !description}
		<span class="truncate font-medium text-secondary-foreground">{title}</span>
	{:else}
		<div class="flex flex-col -space-y-1 overflow-hidden">
			<span class="truncate font-medium text-secondary-foreground">{title}</span>
			<span class="truncate text-xs text-muted-foreground">{description}</span>
		</div>
	{/if}
</a>
