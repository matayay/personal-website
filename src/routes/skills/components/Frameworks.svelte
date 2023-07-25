<script lang="ts">
	import Express from './frameworks/express.svelte';
	import next from './frameworks/next.png';
	import React from './frameworks/react.svelte';
	import Sveltekit from './frameworks/sveltekit.svelte';
	import Tailwind from './frameworks/tailwind.svelte';
</script>

<div class="flex flex-col items-center justify-center gap-2 sm:gap-8">
	<h3 class="text-xl font-bold text-neutral-400 sm:text-2xl md:text-3xl">Frameworks</h3>
	<div class="flex flex-wrap items-center justify-center gap-2 px-4 sm:gap-12">
		<Express />
		<img src={next} alt="Next.js logo" class="h-12 w-12 invert" />
		<React />
		<Sveltekit />
		<Tailwind />
	</div>
</div>
