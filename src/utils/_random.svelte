<script context="module">
	export const randomColor = () => {
		const red	= Math.floor(Math.random() * 256);
		const green	= Math.floor(Math.random() * 256);
		const blue	= Math.floor(Math.random() * 256);
		const alpha = 0.7;

		return (`rgba(${red}, ${green}, ${blue}, ${alpha}`)
	}

	export const randomSize = () => {
		return Math.floor(Math.random() * 60 + 100);
	}

	export const randomNumber = (min, max) => {
		if (min > max) {
			console.log("WARNING: max should bigger than min")
		}
		return Math.random() * (max - min + 1) + min;
	}

	// TODO: 변동을 작게. Math.random()을 곱하는 방법은 0으로 쏠리는 현상이 있음
	// 어떤 분포를 따르게 할 까?
	export const randomLocationWidth = (index) => {
		const weight = 42;
		return weight * index;
	}
	export const randomLocationHeight = (index) => {
		return (parseInt(process.env.HEIGHT, 10) / 2) + 40;
	}
</script>