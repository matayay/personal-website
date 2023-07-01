<script lang="ts">
	import { fade } from 'svelte/transition';
	import { onMount } from 'svelte';

	let transition = false;
	onMount(() => {
		transition = true;
	});
</script>

<div class="min-h-screen bg-black">
	<div class="flex h-[75vh] items-center justify-center">
		<div class="flex flex-col gap-4 sm:gap-8">
			{#if transition}
				<div class="flex gap-4">
					<h2
						in:fade={{ delay: 750, duration: 500 }}
						class="font-mono text-xl text-neutral-300 sm:text-4xl lg:text-6xl"
					>
						Hello There,
					</h2>
					<h2
						in:fade={{ delay: 1500, duration: 500 }}
						class="font-mono text-xl text-neutral-300 sm:text-4xl lg:text-6xl"
					>
						I'm
					</h2>
				</div>

				<h1
					in:fade={{ delay: 2500, duration: 500 }}
					class="font-sans text-4xl text-white sm:text-7xl lg:text-9xl"
				>
					Matayay Karuna
				</h1>
			{/if}
		</div>
	</div>
</div>
