<script context="module">
    import { randomLocationHeight, randomLocationWidth, randomSize } from "../utils/_random.svelte";

	export class Letter extends Path2D {
		constructor(char)
		{
			super();
			this.value = char;
			this.rect(randomLocationWidth(), randomLocationHeight(), randomSize(), randomSize());
		}
	}
</script>