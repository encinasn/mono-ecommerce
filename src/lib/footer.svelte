<script>
	const sections = [
		{
			title: 'Help',
			links: ['Customer service', 'FAQ', 'My Orders', 'Contect Us', 'Product Recalls']
		},
		{
			title: 'Company',
			links: ['About', 'News', 'Contacts', 'Careers', 'Retailers']
		},
		{
			title: 'Legal',
			links: ['Legal notice', 'Terms of sale', 'Privacy policy', 'Cookie policy']
		},
		{
			title: 'Connect',
			links: ['Instagram', 'Facebook', 'Telegram', 'Pinterest', 'Tik Tok']
		}
	];
</script>

<footer class="bg-neutral-900 text-white w-full flex justify-center">
	<div class="max-w-screen-lg w-full grid lg:grid-cols-6 gap-8 my-24">
		<section class="col-span-2 h-full flex flex-col justify-between">
			<h2 class="logo text-lg">mono</h2>

			<p class="text-sm mt-6 text-neutral-100 lg:w-[80%]">
				Curiosity, courage and creativity —
				<br /> MONO is here to do things diferently for the life you live
			</p>

			<p class="text-neutral-400 text-sm mt-auto">© MONO. All rights reserved.</p>
		</section>

		{#each sections as section}
			<section>
				<h3 class="uppercase text-sm font-medium">{section.title}</h3>

				<ul class="flex flex-col gap-3 mt-6">
					{#each section.links as link}
						<li class="text-neutral-400 text-sm hover:underline underline-offset-2">
							<a href="/#">{link}</a>
						</li>
					{/each}
				</ul>
			</section>
		{/each}
	</div>
</footer>
