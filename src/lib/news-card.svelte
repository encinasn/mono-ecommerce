<script lang="ts">
	export let data: {
		image?: string;
		title: string;
		description?: string;
		category: string;
		createdAt: string;
	};
</script>

<li class="group first:border-none border-b first:row-span-3 pb-6 first:pb-0 border-neutral-200">
	<picture class="aspect-video w-full h-auto hidden group-first:block bg-neutral-100">
		<img src={data.image} alt={data.title} class="object-cover h-full" />
	</picture>

	<div class="group-first:mt-4">
		<div class="flex gap-4 text-xs text-neutral-600">
			<p>{data.category}</p>
			<p>{data.createdAt}</p>
		</div>

		<h3 class="text-2xl leading-relaxed mt-2 font-semibold font-heading">
			{data.title}
		</h3>
	</div>

	<p class="hidden group-first:[display:-webkit-box] line-clamp-4 text-sm text-neutral-600 mt-4">
		{data.description}
	</p>
</li>
