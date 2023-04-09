<script>
	import CategoryCard from '$lib/category-card.svelte';
	import Carousel from '$lib/carousel.svelte';
	import NewsCard from '$lib/news-card.svelte';
	import ProductCard from '$lib/product-card.svelte';

	const news = [
		{
			image: '/news.png',
			category: 'Advise',
			createdAt: 'Aug 28, 2022',
			title: 'How to choose the right sofa for your interior?',
			description:
				'Furniture from Italy has many distinctive advantages. The high cost of branded Italian headsets and individual items is fully justified by the quality and durability. A special approach to production allows manufacturers to achieve such results. Creating durable and wear-resistant furniture'
		},
		{
			category: 'Advise',
			createdAt: 'Sep 01, 2022',
			title:
				'On the other hand, we denounce with rigtheous indignation and dislike men who are so beguiled'
		},
		{
			category: 'News',
			createdAt: 'Oct 17, 2022',
			title:
				'We invite you to read the offer of the most innovate manufacturer of premium upholstered furniture in Europe'
		},
		{
			category: 'News',
			createdAt: 'Dec 23, 2022',
			title:
				'Eco-leather furniture care instructions. Indignation and dislike men who are so beguiled'
		}
	];

	let images = [
		'/carousel/alpha.png',
		'/carousel/beta.png',
		'/carousel/charlie.png',
		'/carousel/delta.png',
		'/carousel/echo.png'
	];
</script>

<section class="flex justify-center">
	<div class="max-w-screen-lg w-full mt-24">
		<div class="flex justify-between items-center">
			<h2 class="section-title">Hot Products</h2>

			<a href="/#" class="underline uppercase text-sm underline-offset-2 font-medium">See All</a>
		</div>

		<ul class="hot-products-grid mt-8">
			<ProductCard />
			<ProductCard />
			<ProductCard />
			<ProductCard />
			<ProductCard />
		</ul>
	</div>
</section>

<section class="grid grid-cols-6 grid-rows-3 gap-5 mt-32">
	<picture class="block col-span-3 row-span-2 w-full h-full overflow-hidden bg-neutral-100">
		<img src="/categories-large.png" alt="" class="object-cover" />
	</picture>

	<CategoryCard
		image="/categories/sofas.png"
		name="Sofas"
		description="It is important to provide a unique combination of exterior finishes, functionality, design interior and construction."
	/>
	<CategoryCard
		image="/categories/chairs.png"
		name="Chairs"
		description="We offer premium class furniture from the best European factories for connoisseurs of hight interior style."
	/>
	<div />
	<div />
	<CategoryCard
		image="/categories/tables.png"
		name="Tables"
		description="On sale - exclusive furniture for living rooms bedrooms and kitchens, offices, lighting fixtures and interior decor items."
	/>
	<picture class="block col-span-3 w-full h-full overflow-hidden bg-neutral-100">
		<img src="/categories-small.png" alt="" class="object-cover" />
	</picture>
</section>

<section class="flex justify-center">
	<div class="max-w-screen-lg w-full mt-24">
		<h2 class="section-title">Our News</h2>

		<ul class="grid grid-cols-2 grid-rows-[auto_auto_auto] gap-x-10 gap-y-6 mt-8">
			{#each news as data}
				<NewsCard {data} />
			{/each}
		</ul>
	</div>
</section>

<section class="flex justify-center">
	<div class="max-w-screen-lg w-full my-32">
		<Carousel autoplay={2000}>
			<li class="aspect-square overflow-hidden w-56 h-56 flex flex-col justify-center p-3">
				<p class="text-3xl font-semibold font-heading">@monostyle</p>

				<p class="text-sm text-neutral-600 mt-2">
					Immerse yourself in the magnifia esthetics of our interiors and feel of our furniture.
				</p>

				<a href="/#" class="uppercase underline text-sm font-medium mt-4 block underline-offset-2"
					>Go to instagram</a
				>
			</li>

			{#each images as image, index (index)}
				<li class="aspect-square min-w-max overflow-hidden w-56 h-56 bg-neutral-100">
					<img src={image} alt="" class="object-cover" />
				</li>
			{/each}
		</Carousel>
	</div>
</section>

<style lang="postcss">
	.hot-products-grid {
		--gap: 1.25rem;
		--img-height: 14.1rem;
		--caption-height: 3.7rem;
		--large-col: calc(var(--img-height) * 2 + var(--caption-height) + var(--gap));
		display: grid;
		grid-template-columns: var(--large-col) var(--img-height) var(--img-height);
		grid-template-rows: auto auto;
		gap: var(--gap);
	}
</style>
