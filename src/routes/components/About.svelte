<script lang="ts">
	import { fade } from 'svelte/transition';
	import { onMount } from 'svelte';
	import me from '../../libs/assets/me.jpeg';

	let transition = false;
	onMount(() => {
		transition = true;
	});
</script>

<div class="h-screen">
	<div
		class="flex h-3/4 w-full flex-col items-center justify-center gap-6 sm:flex-row sm:justify-evenly sm:gap-0"
	>
		<div class="flex flex-col gap-4 sm:gap-8">
			{#if transition}
				<div class="flex gap-4">
					<h2
						in:fade={{ delay: 750, duration: 500 }}
						class="font-mono text-lg text-neutral-300 sm:text-2xl lg:text-5xl"
					>
						Hello There,
					</h2>
					<h2
						in:fade={{ delay: 1500, duration: 500 }}
						class="font-mono text-lg text-neutral-300 sm:text-2xl lg:text-5xl"
					>
						I'm
					</h2>
				</div>

				<h1
					in:fade={{ delay: 2500, duration: 500 }}
					class="font-sans text-3xl text-white sm:text-5xl lg:text-8xl"
				>
					Matayay Karuna
				</h1>
			{/if}
		</div>

		{#if transition}
			<div
				in:fade={{ delay: 3500, duration: 1500 }}
				class="sm:items-centers flex w-64 items-start justify-center gap-2 rounded-xl
						bg-gradient-to-tl from-sky-950 p-6 sm:flex-col sm:gap-8 sm:p-8 md:w-80 xl:w-[38rem]"
			>
				<div class="flex w-full items-center justify-center">
					<img src={me} alt="Matayay" class="h-auto w-80 rounded-full" />
				</div>
				<article class="flex flex-col gap-4">
					<h3 class="text-lg text-neutral-300 sm:text-2xl">A little about me</h3>
					<p class="text-sm text-gray-400 xl:text-xl">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
						incididunt ut labore et dolore magna aliqua. Feugiat vivamus at augue eget arcu dictum
						varius.
					</p>
				</article>
			</div>
		{/if}
	</div>
</div>
