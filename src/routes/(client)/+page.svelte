<script lang="ts">
	import Category from './Category.svelte'
	import { BadgePlus } from 'lucide-svelte'
	import ChipLink from './ChipLink.svelte'
	import { Button } from '$lib/components/ui/button'
</script>

<div class="w-full rounded-2xl bg-red-500 px-6 py-4">
	<h1 class="font-heading text-3xl font-bold text-white">Heartwork</h1>
</div>

<div class="mt-12 flex flex-col space-y-16">
	<Category title="Activity Presets Logging" seeMoreLink="/">
		<div class="grid grid-cols-2 gap-6 md:grid-cols-4 lg:grid-cols-5">
			<ChipLink title="Coding" />
			<ChipLink title="Hospital ER" />
			<ChipLink title="Food Bank" />
			<ChipLink title="Pink-Out Week" />
			<ChipLink title="Computer repair" />
		</div>
	</Category>
	<Category title="Organizations" seeMoreLink="/">
		<div class="grid grid-cols-2 gap-6 md:grid-cols-4 lg:grid-cols-5">
			<ChipLink title="OMRF" />
			<ChipLink title="Hospital ER" />
			<ChipLink title="Food Bank" />
			<ChipLink title="Log Hours" />
			<ChipLink title="Log Hours" />
		</div>
	</Category>
</div>
