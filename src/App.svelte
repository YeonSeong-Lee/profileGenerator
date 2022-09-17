<script>
	import ImageGenerator from "./ImageGenerator.svelte";
	let name;
</script>

<main>
	<ImageGenerator name={name}/>
	<p>make your team's profile</p>
	<input type='text' bind:value={name} />
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
</style>