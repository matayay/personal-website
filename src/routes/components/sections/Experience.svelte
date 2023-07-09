<script lang="ts">
	import { onMount } from 'svelte';
	import Lair from '../content/LAIR.svelte';

	let index = 0;
	let styles = [true, false, false];

	const handleClick = (i: number) => {
		index = i;
		for (let j = 0; j < styles.length; j++) {
			styles[j] = false;
		}
		styles[i] = true;
	};
</script>

<section
	class="flex min-h-screen flex-col items-center gap-10 bg-gradient-to-t from-slate-950 pt-20"
	id="experience"
>
	<div class="flex w-full flex-col items-center justify-center gap-4">
		<h2 class="text-center text-2xl text-neutral-300 sm:text-5xl">My Work Experience</h2>
		<div class="h-1 w-3/4 rounded-3xl bg-gray-400" />
	</div>

	<div class="flex max-w-full flex-col items-center justify-center rounded-3xl bg-gray-900 p-8">
		<div class="flex w-full items-center justify-center">
			<nav class="mb-2 flex items-center justify-start overflow-x-scroll pb-2">
				<button
					class={`flex flex-col items-center justify-center gap-2 bg-white pt-2 ${
						styles[0] ? 'bg-opacity-5' : 'bg-opacity-0'
					}`}
					on:click={() => handleClick(0)}
				>
					<h3 class={`w-max px-6 ${styles[0] ? 'text-cyan-500' : 'text-neutral-400'}`}>
						CU LAIR Lab
					</h3>
					<div class={`h-0.5 w-full ${styles[0] ? 'bg-cyan-500' : 'bg-slate-600'}`} />
				</button>

				<button
					class={`flex flex-col items-center justify-center gap-2 bg-white pt-2 ${
						styles[1] ? 'bg-opacity-5' : 'bg-opacity-0'
					}`}
					on:click={() => handleClick(1)}
				>
					<h3 class={`w-max px-6 ${styles[1] ? 'text-cyan-500' : 'text-neutral-400'}`}>Job 2</h3>
					<div class={`h-0.5 w-full ${styles[1] ? 'bg-cyan-500' : 'bg-slate-600'}`} />
				</button>

				<button
					class={`flex flex-col items-center justify-center gap-2 bg-white pt-2 ${
						styles[2] ? 'bg-opacity-5' : 'bg-opacity-0'
					}`}
					on:click={() => handleClick(2)}
				>
					<h3 class={`w-max px-6 ${styles[2] ? 'text-cyan-500' : 'text-neutral-400'}`}>Job 1</h3>
					<div class={`h-0.5 w-full ${styles[2] ? 'bg-cyan-500' : 'bg-slate-600'}`} />
				</button>
			</nav>
		</div>

		{#if index === 0}
			<Lair />
		{:else}
			<h1>Bruh</h1>
		{/if}
	</div>
</section>
