<script context="module">
    import { Letter } from "./_Letter.svelte";

	export const drawLetter = (name, ctx, canvas) => {
		const letter = new Letter(name[name.length - 1], canvas.width, canvas.height);
		ctx.fillStyle = "rgb(200, 0, 0)"
		ctx.stroke(letter);
	}
</script>