<script context="module">
    import { init } from "svelte/internal";
    import { randomLocationHeight, randomLocationWidth, randomSize } from "../utils/_random.svelte";

	export class Letter extends Path2D {
		constructor(char, x, y)
		{
			super();
			this.x;
			this.y;
			this.value;
			this.init(char, x, y);
		}

		init(char, x, y) {
			this.value = char;
			this.x = x ;
			this.y = y;
		}

		drawRect() {
			this.rect(this.x, this.y, 42, 42);
		}

		get x() {
			return this._x;
		}

		set x(value) {
			if (value >= parseInt(process.env.WIDTH, 10) - 42) {
				this._x = parseInt(process.env.WIDTH, 10) - 42;
				return;
			}
			this._x = value;
		}
	}
</script>