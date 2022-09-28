<script context="module">
    import { Letter } from "./_Letter.svelte";
    import { randomColor } from "../../utils/_random.svelte";

	function sleep(sec) {
  		return new Promise(resolve => setTimeout(resolve, sec * 1000));
	} 

	export const drawLetter = async (name, ctx) => {
		ctx.fillStyle = randomColor();
		let letter = new Letter(ctx, name[name.length - 1], 0, 0);
		letter.drawValue();
	}
</script>