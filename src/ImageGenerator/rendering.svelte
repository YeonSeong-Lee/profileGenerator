<script context="module">
	export const rendering = (name) => {
		const canvas = document.getElementById("profileGenerator");
        if (!canvas.getContext)
		return alert('use other broswer');
        const ctx = canvas.getContext("2d");
		ctx.fillStyle = "rgb(200, 0, 0)";
		ctx.fillRect(10, 10, 50, 50);
		ctx.fillStyle = "rgba(0, 0, 200, 0.5)";
        ctx.fillRect(30, 30, 50, 50);
		ctx.font = 'bold 48px serif';
		ctx.strokeText(`${name}`, 50, 100);
	}
</script>