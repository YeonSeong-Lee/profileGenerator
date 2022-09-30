<script context="module">
	import { randomColor, randomSize } from "../../utils/_random.svelte";

	export class Letter extends Path2D {
		constructor(ctx, char, x, y, index)
		{
			super();
			this.x;
			this.y;
			this.index;
			this.ctx;
			this.value;
			this.init(ctx, char, x, y, index);
		}
		// TODO: init 인자 순서 정리
		init(ctx, char, x, y, index) {
			this.ctx = ctx;
			this.value = char;
			this.x = x ;
			this.y = y;
			this.index = index;
		}

		drawRect() {
			this.rect(this.x, this.y, 42, 42);
			this.ctx.fillStyle = randomColor();
			this.ctx.shadowColor = "black";
			this.ctx.fill(this);
		}
	// TODO: 구분선의 색 정하기. -> 아마 보색..? 검정색..?
		drawValue() {
			this.ctx.fillStyle = randomColor();
			this.ctx.strokeStyle = randomColor();
			this.ctx.shadowColor = "black";
			this.ctx.font = `${randomSize()}px Arial`;
			this.ctx.fillText(this.value, this.x, this.y);
			this.ctx.strokeText(this.value, this.x, this.y);
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