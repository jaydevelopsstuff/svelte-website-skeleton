<script>
	import Header from "$lib/Header.svelte";
	import Footer from "$lib/Footer.svelte";
</script>

<div class="app">
	<div class="container">
		<Header />
		<main class="main">
			<slot />
		</main>
		<Footer />
	</div>
</div>

<style>
	.app {
		background-color: var(--theme-background);
		display: flex;
		justify-content: center;
	}
	.container {
		width: 80vw;
	}
</style>