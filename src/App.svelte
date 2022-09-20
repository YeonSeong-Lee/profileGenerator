<script>
	import ImageGenerator from "./ImageGenerator.svelte";
	import Header from "./Header.svelte";
	import Footer from "./Footer.svelte";
	let name;
</script>

<Header />
<main>
	<ImageGenerator name={name}/>
	<p>make your team's profile</p>
	<input type='text' bind:value={name} />
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