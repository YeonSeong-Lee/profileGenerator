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
</script>