<script lang="ts">
	export let name: string;
	export let description: string;
	export let image: string;
</script>

<div class="grid grid-cols-2 col-span-2 group gap-5 grid-flow-col">
	<picture class="block aspect-square w-full h-auto overflow-hidden bg-neutral-100">
		<img src={image} alt={name} class="object-cover" />
	</picture>

	<div class="flex flex-col justify-center group-first-of-type:col-[1]">
		<h3 class="text-4xl font-semibold font-heading">{name}</h3>
		<p class="text-sm text-neutral-600 mt-4">{description}</p>
		<a href="/#" class="uppercase underline text-sm font-medium mt-4 block underline-offset-2"
			>Catalog</a
		>
	</div>
</div>
