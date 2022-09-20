<script context="module">
	export const drawLetter = (name, ctx, canvas) => {
		ctx.strokeText(`${name}`, Math.random() * canvas.width, Math.random() * canvas.height);
	}
</script>