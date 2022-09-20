<script>
	import ImageGenerator from "./ImageGenerator/ImageGenerator.svelte";
	import Header from "./Header.svelte";
	import Footer from "./Footer.svelte";
	let inputValue;
</script>

<Header />
<main>
	<ImageGenerator name={inputValue}/>
	<p>make your team's profile</p>
	<input type='text' bind:value={inputValue} />
</main>
<Footer />

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>