<script context="module">
    import { Letter } from "./_Letter.svelte";
    import { randomColor } from "../utils/_random.svelte";

	export const drawLetter = (name, ctx) => {
		for (let i = 0; i < 42; i++) {
			const letter = new Letter(name[name.length - 1]);
			ctx.fillStyle = randomColor();
			ctx.fill(letter);
		}
	}
</script>