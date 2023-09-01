<script>
	import { parse, renderHTML } from '@djot/djot';

	export let text = '';

	const doc = parse(text);
	const html = renderHTML(doc);
</script>

{@html html}
