<script>
	export let name;
</script>

<div>
	{#if name}
		<h1>{name}</h1>
	{:else}
		<h1>defalut image</h1>
{/if}
</div>

<style>
	h1 {
			color: #ff3e00;
			text-transform: uppercase;
			font-size: 4em;
			font-weight: 100;
		}

		@media (min-width: 640px) {
			div {
				max-width: none;
			}
		}
</style>