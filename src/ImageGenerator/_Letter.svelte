<script context="module">
    import { randomSize } from "../utils/_random.svelte";


	export class Letter extends Path2D {
		constructor(char, max_width, max_height)
		{
			super();
			this.value = char;
			this.rect(max_width * Math.random(),  max_height * Math.random(),randomSize(), randomSize());
		}
	}
</script>