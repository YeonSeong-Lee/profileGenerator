<script context="module">
    import { Letter } from "./_Letter.svelte";
    import { randomColor, randomLocationHeight, randomLocationWidth } from "../../utils/_random.svelte";

	export const drawLetter = (name, ctx) => {
		// TODO: 글자에 색입히기
		// TODO: 몇번째 인덱스인지에 따라 위치 달라지게
		// TODO: delete 버튼 눌렀을 때, 마지막 인덱스 지우기
		let letter = new Letter(ctx, name[name.length - 1], randomLocationWidth(name.length - 1), randomLocationHeight(name.length - 1), name.length - 1);
		console.log("🚀 ~ file: _drawLetter.svelte ~ line 8 ~ drawLetter ~ letter", letter)
		letter.drawValue();
	}
</script>