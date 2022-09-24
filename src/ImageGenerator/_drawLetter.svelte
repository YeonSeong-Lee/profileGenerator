<script context="module">
    import { Letter } from "./_Letter.svelte";
    import { randomRGB } from "../utils/_random.svelte";

	export const drawLetter = (name, ctx) => {
		const letter = new Letter(name[name.length - 1]);
		ctx.fillStyle = randomRGB();
		ctx.fill(letter);
	}
</script>