<script context="module" lang="ts">
	import { parse, renderHTML } from '@djot/djot';
	export type HTMLRenderOptions = Parameters<typeof renderHTML>[1];
</script>

<script lang="ts">
	export let text = '';
	export let options: HTMLRenderOptions = undefined;

	const doc = parse(text);
	const html = renderHTML(doc, options);
</script>

{@html html}
