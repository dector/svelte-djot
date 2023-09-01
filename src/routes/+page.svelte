<script>
	// import { Djot } from '$lib/index.js';
	import { Djot } from 'svelte-djot';

	const text = '{-Hello-} {+Hola+} _djot_ from *SvelteKit*!';
</script>

<Djot {text} />
