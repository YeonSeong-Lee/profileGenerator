<script context="module">
    import { Letter } from "./_Letter.svelte";
    import { randomRGB } from "./_randomRGB.svelte";

	export const drawLetter = (name, ctx, canvas) => {
		const letter = new Letter(name[name.length - 1], canvas.width, canvas.height);
		ctx.fillStyle = randomRGB();
		ctx.fill(letter);
	}
</script>