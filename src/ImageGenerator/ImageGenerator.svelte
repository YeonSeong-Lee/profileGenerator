<script>
	import { beforeUpdate, tick } from 'svelte';
	export let name;
	import { rendering } from "./rendering.svelte"
	
	beforeUpdate(async() => {
		await tick();
		rendering(name);
	})
</script>

<div>
	<canvas id="profileGenerator" width="400" height="400"></canvas>
</div>

<style>
    canvas {
        border: 1px solid black;
      }
</style>