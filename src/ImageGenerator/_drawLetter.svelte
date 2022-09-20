<script context="module">
	export const drawLetter = (name, ctx, canvas) => {
		ctx.strokeText(`${name[name.length - 1]}`, Math.random() * canvas.width, Math.random() * canvas.height);
	}
</script>