<script context="module">
	import { drawLetter } from "./_drawLetter.svelte";

	export const rendering = (name) => {
		const canvas = document.getElementById("profileGenerator");
        if (!canvas.getContext)
			return alert('use other broswer');	
		const ctx = canvas.getContext("2d");
		if (!name) {
			ctx.clearRect(0, 0, canvas.width, canvas.height);
			return ;
		}
		drawLetter(name, ctx);
	}
</script>