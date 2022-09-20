<script context="module">
	export const rendering = (name) => {
		const canvas = document.getElementById("profileGenerator");
        if (!canvas.getContext)
			return alert('use other broswer');	
		const ctx = canvas.getContext("2d");
		if (!name) {
			ctx.clearRect(0, 0, canvas.width, canvas.height);
			return ;
		}
		ctx.font = 'bold 42px serif';
		ctx.strokeText(`${name}`, 50, 100);
	}
</script>