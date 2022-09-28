<script>
	import ImageGenerator from "./ImageGenerator/ImageGenerator.svelte";

	let inputValue;
	let displayValue;
	const keyup_handler = (event) => {
		if (inputValue && (event?.key === 'Backspace' || event?.key === 'Delete'))
			return ;
		displayValue = inputValue;
	}
</script>

<main>
	<ImageGenerator name={displayValue}/>
	<p>make your team's profile</p>
	<input type='text' bind:value={inputValue} on:keyup={keyup_handler}/>
</main>

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