<script>
	let name;
</script>

<main>
	{#if name}
		<h1>{name}</h1>
	{:else}
		<h1>defalut image</h1>
	{/if}
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

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>