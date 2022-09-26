<script context="module">
    import { Letter } from "./_Letter.svelte";
    import { randomColor } from "../utils/_random.svelte";

	export const moveLetterX = (letter, ctx, step) => {
		ctx.clearRect(0, 0, process.env.WIDTH, process.env.HEIGHT);
		letter.setX(letter.getX() + step)
		letter.drawRect();
		ctx.fill(letter);
	}

	export const drawLetter = (name, ctx) => {
		const letter = new Letter(name[name.length - 1]);
		ctx.fillStyle = randomColor();
		letter.drawRect();
		ctx.fill(letter);
		for (let i = 0; i < 42; i++) {
			moveLetterX(letter, ctx, 20);
			setTimeout(()=>{}, 3000);
		}
	}
</script>