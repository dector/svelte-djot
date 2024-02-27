<script lang="ts">
	import { Djot } from '$lib/index.js';
  import type { HTMLRenderOptions } from '$lib/Djot.svelte';
		
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
