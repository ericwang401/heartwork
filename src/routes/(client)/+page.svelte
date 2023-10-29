<script lang="ts">
	import Category from './Category.svelte'
	import { BadgePlus, Heart } from 'lucide-svelte'
	import ActivityLink from './ActivityLink.svelte'
	import { Button } from '$lib/components/ui/button'
	import HeartShapedHandShake from '$lib/components/icons/HeartShapedHandShake.svelte'
	import OrganizationLink from './OrganizationLink.svelte'
</script>

<div class="flex w-full items-center space-x-4 rounded-2xl py-4">
	<HeartShapedHandShake class="w-12 mt-1 text-red-600" />
	<h1 class="font-heading text-3xl font-bold text-red-600">Heartwork</h1>
</div>

<div class="mt-12 flex flex-col space-y-16">
	<Category title="Activities" seeMoreLink="/">
		<div class="grid grid-cols-2 gap-6 md:grid-cols-4 lg:grid-cols-5">
			<ActivityLink title="Coding" />
			<ActivityLink title="Hospital ER" />
			<ActivityLink title="Food Bank" />
			<ActivityLink title="Pink-Out Week" />
			<ActivityLink title="Computer repair" />
		</div>
	</Category>
	<Category title="Organizations" seeMoreLink="/">
		<div class="grid grid-cols-2 gap-6 md:grid-cols-4 lg:grid-cols-5">
			<OrganizationLink title="OMRF" />
			<OrganizationLink title="Hospital ER" />
			<OrganizationLink title="Food Bank" />
			<OrganizationLink title="Log Hours" />
			<OrganizationLink title="Log Hours" />
		</div>
	</Category>
</div>
