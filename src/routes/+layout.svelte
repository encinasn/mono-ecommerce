
<script>
	// @ts-nocheck
	import '../app.css';
	
	import Footer from '$lib/footer.svelte';
	import Header from '$lib/header.svelte';
</script>

<svelte:head>
	<title>MONO</title>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Darker+Grotesque:wght@400;500;600;700;800&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<Header />
<main class="min-h-[calc(100vh-5rem)] antialiased">
	<slot />
</main>
<Footer />

<style lang="postcss">
	:global(html) {
		background-color: theme(colors.gray.50);
		font-family: 'Inter';
	}
</style>
