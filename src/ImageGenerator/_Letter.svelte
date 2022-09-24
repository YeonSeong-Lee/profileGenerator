<script context="module">
    import { randomSize } from "../utils/_random.svelte";

	export class Letter extends Path2D {
		constructor(char)
		{
			super();
			this.value = char;
			this.rect(process.env.WIDTH * Math.random(),  process.env.HEIGHT * Math.random(), randomSize(), randomSize());
		}
	}
</script>