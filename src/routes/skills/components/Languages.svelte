<script lang="ts">
	import Cpp from './languages/cpp.svelte';
	import Css from './languages/css.svelte';
	import Html from './languages/html.svelte';
	import Javascript from './languages/javascript.svelte';
	import Python from './languages/python.svelte';
</script>

<div class="flex flex-col items-center justify-center gap-2 sm:gap-8">
	<h3 class="text-xl font-bold text-neutral-400 sm:text-2xl md:text-3xl">Languages</h3>
	<div class="flex flex-wrap items-center justify-center gap-2 px-4 sm:gap-12">
		<Cpp />
		<Css />
		<Html />
		<Javascript />
		<Python />
	</div>
</div>
