<script>
	import { onMount } from 'svelte';

	const rendering = (name) => {
		const canvas = document.getElementById("profileGenerator");
        if (!canvas.getContext)
			return alert('use other broswer');
        const ctx = canvas.getContext("2d");
		ctx.fillStyle = "rgb(200, 0, 0)";
		ctx.fillRect(10, 10, 50, 50);
		ctx.fillStyle = "rgba(0, 0, 200, 0.5)";
        ctx.fillRect(30, 30, 50, 50);
		ctx.font = 'bold 48px serif';
		ctx.strokeText(`${name}`, 50, 100);
	}
	// 랜더링 함수 만든 뒤에, mount될 때, 인풋에서 글자가 입력될 때 랜더링하게 하기
	onMount(async (name) => {
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