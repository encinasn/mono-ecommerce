<script>
	import Icon from './icon.svelte';
</script>

<header class="w-full flex justify-center bg-neutral-900">
	<nav class="w-full grid items-center lg:grid-cols-3 h-20 max-w-screen-lg text-white">
		<div>
			<h2 class="logo text-lg">Mono</h2>
		</div>
		<div class="flex gap-3 uppercase text-sm justify-center">
			<a class="hover:underline underline-offset-2" href="/#">Shop</a>
			<a class="hover:underline underline-offset-2" href="/#">Inspiration</a>
			<a class="hover:underline underline-offset-2" href="/#">About</a>
			<a class="hover:underline underline-offset-2" href="/#">Contacts</a>
		</div>

		<div class="flex justify-end">
			<a href="/#" class="w-10 h-10 text-white flex items-center justify-center"
				><Icon type="search" /></a
			>
			<a href="/#" class="w-10 h-10 flex items-center justify-center"><Icon type="cart" /></a>
		</div>
	</nav>
</header>
