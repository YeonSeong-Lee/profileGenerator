<script context="module">
    import { randomLocationHeight, randomLocationWidth, randomSize } from "../utils/_random.svelte";

	export class Letter extends Path2D {
		constructor(char)
		{
			super();
			this.x = randomLocationWidth();
			this.y = randomLocationHeight();
			this.value = char;
		}
		drawRect() {
			this.rect(this.x, this.y, randomSize(), randomSize());
		}
		setX(num) {
			this.x = num;
		}
		setY(num) {
			this.y = num;
		}
		getX() {
			return this.x;
		}
		getY() {
			return this.y;
		}
	}
</script>