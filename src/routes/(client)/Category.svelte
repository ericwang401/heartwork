<script lang="ts">
	import { Button } from '$lib/components/ui/button'

	export let title: string
	export let seeMoreLink: string | null | undefined = null
</script>

<section class="flex flex-col space-y-6">
	{#if !seeMoreLink}
		<h2 class="font-heading text-2xl font-bold">{title}</h2>
	{:else}
		<div class="flex justify-between">
			<h2 class="font-heading text-2xl font-bold">{title}</h2>
            <Button variant="ghost" href={seeMoreLink}>See more</Button>
		</div>
	{/if}
	<slot />
</section>
