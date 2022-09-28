<script context="module">
    import { Letter } from "./_Letter.svelte";
    import { randomColor } from "../utils/_random.svelte";

	function sleep(sec) {
  return new Promise(resolve => setTimeout(resolve, sec * 1000));
} 
	export const drawLetter = async (name, ctx) => {
		ctx.fillStyle = randomColor();
		ctx.fillStyle = randomColor();
		let letter = new Letter(name[name.length - 1], 4, 2);
		for (let i = 0; i < 42; i++) {
			ctx.clearRect(0, 0, process.env.WIDTH, process.env.HEIGHT);
			let new_letter = new Letter(name[name.length - 1], parseInt(letter.x + 42 * i, 10), letter.y + 42)
			new_letter.drawRect();
			ctx.fill(new_letter);
			await sleep(0.1);
		}
		for (let i = 0; i < 42; i++) {
			ctx.clearRect(0, 0, process.env.WIDTH, process.env.HEIGHT);
			let new_letter = new Letter(name[name.length - 1], parseInt(letter.x + 42, 10), letter.y + 42 * i)
			new_letter.drawRect();
			ctx.fill(new_letter);
			await sleep(0.1);
		}
	}
</script>