<script context="module">
	// TODO: 요소들 객체화 하기
	export const drawLetter = (name, ctx, canvas) => {
		ctx.font = 'bold 60px serif';
		ctx.strokeText(`${name[name.length - 1]}`, Math.random() * canvas.width, Math.random() * canvas.height);
	}
</script>