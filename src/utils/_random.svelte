<script context="module">
	export const randomRGB = () => {
		const red	= Math.floor(Math.random() * 256);
		const green	= Math.floor(Math.random() * 256);
		const blue	= Math.floor(Math.random() * 256);

		return (`rgb(${red}, ${green}, ${blue}`)
	}

	export const randomSize = () => {
		return Math.floor(Math.random() * 60 + 5);
	}

	export const randomLocationWidth = () => {
		return Math.floor(Math.random() * (parseInt(process.env.WIDTH, 10) + 1))
	}
	export const randomLocationHeight = () => {
		return Math.floor(Math.random() * (parseInt(process.env.HEIGHT, 10) + 1))
	}
</script>