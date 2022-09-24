<script>
	import { beforeUpdate, tick } from 'svelte';
	export let name;
	import { rendering } from "./_rendering.svelte"
	beforeUpdate(async() => {
		await tick();
		rendering(name);
	})
</script>

<div>
	<canvas id="profileGenerator" width = process.env.WIDTH height = process.env.HEIGHT></canvas>
</div>

<style>
    canvas {
        border: 1px solid black;
      }
</style>