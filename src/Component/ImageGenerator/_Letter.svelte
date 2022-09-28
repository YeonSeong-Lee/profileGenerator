<script context="module">
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
			this._x = placeInCanvas(value);
		}

		get y() {
			return this._y;
		}

		set y(value) {
			this._y = placeInCanvas(value);
		}
	}

	const placeInCanvas = (value) => {
			const max_width = parseInt(process.env.WIDTH, 10);
			if (value < max_width && value >= 0) {
				return value;
			}
			if (value >= max_width) {
				return placeInCanvas(2 * (max_width - 42) - value);
			}
			if (value < 0) {
				return placeInCanvas(-value);
			}
	}
</script>