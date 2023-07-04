<script lang="ts">
	import { fade } from 'svelte/transition';
	import { onMount } from 'svelte';
	import me from '../../../libs/assets/me.jpeg';

	let transition = false;
	onMount(() => {
		transition = true;
	});
</script>

<div class="h-screen" id="about">
	<div
		class="flex h-3/4 w-full flex-col items-center justify-center gap-6 sm:flex-row sm:justify-evenly sm:gap-0"
	>
		<div class="flex flex-col gap-4 sm:gap-8">
			{#if transition}
				<div class="flex gap-4">
					<h2
						in:fade={{ delay: 750, duration: 500 }}
						class="font-mono text-lg text-neutral-300 sm:text-xl lg:text-4xl"
					>
						Hello There,
					</h2>
					<h2
						in:fade={{ delay: 1500, duration: 500 }}
						class="font-mono text-lg text-neutral-300 sm:text-xl lg:text-4xl"
					>
						I'm
					</h2>
				</div>

				<h1
					in:fade={{ delay: 2500, duration: 500 }}
					class="font-sans text-3xl text-white sm:text-4xl lg:text-7xl"
				>
					Matayay Karuna
				</h1>
			{/if}
		</div>

		{#if transition}
			<div
				in:fade={{ delay: 3500, duration: 1500 }}
				class="sm:items-centers flex w-64 flex-col items-start justify-center gap-2
						rounded-xl bg-gradient-to-tl from-sky-950 p-4 sm:w-80 xl:w-[38rem] xl:gap-10 xl:p-8"
			>
				<div class="flex w-full items-center justify-center">
					<img src={me} alt="Matayay" class="h-auto w-16 rounded-full md:w-28 xl:w-48" />
				</div>
				<article class="flex flex-col gap-1 lg:gap-4">
					<h3 class="text-lg text-neutral-300 lg:text-2xl">A little about me</h3>
					<p class="text-sm text-gray-400 sm:text-xs xl:text-xl">
						I'm an aspiring developer and current CS student at CU Boulder. I have a passion for
						learning and am always looking to discover something new. Some of my hobbies outside
						tech are skiing, video games, and long walks in nature.
					</p>
				</article>
			</div>
		{/if}
	</div>
</div>
