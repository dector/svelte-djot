<script lang="ts">
	import { Djot } from '$lib/index.js';
  import type { renderHTML } from '@djot/djot';
		
	type HTMLRenderOptions = Parameters<typeof renderHTML>[1];

	const text = '{-Hello-} {+Hola+} _djot_ from *SvelteKit*!';

  const options: HTMLRenderOptions = {
    overrides: {
      emph: (node, renderer) => {
        return `<span style="background-color: yellow;">${renderer.renderChildren(node)}</span>`
      }
    }
  }
</script>

<Djot {text} {options} />
