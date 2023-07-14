<script lang="ts">
	import Lair from './components/LAIR.svelte';
	import { inview } from 'svelte-inview';

	let index = 0;
	let styles = [true, false, false];
	let isInView: boolean;

	const handleClick = (i: number) => {
		index = i;
		for (let j = 0; j < styles.length; j++) {
			styles[j] = false;
		}
		styles[i] = true;
	};
</script>

<div
	class="wrapper"
	use:inview={{ unobserveOnEnter: true, rootMargin: '-25%' }}
	on:inview_change={(event) => {
		const { inView, entry, scrollDirection, observer, node } = event.detail;
		isInView = inView;
	}}
>
	<div class="bg-gradient-to-tr from-[#0a192f]">
		<section
			class={`flex flex-col items-center pt-20 duration-1000 ease-in ${
				isInView ? 'opacity-100' : 'opacity-0'
			}`}
			id="experience"
		>
			<div class="flex w-full flex-col items-center justify-center gap-1 lg:gap-4">
				<h2 class="text-center text-2xl text-neutral-300 xl:text-5xl">My Work Experience</h2>
				<div class="h-1 w-3/4 rounded-3xl bg-gray-800" />
			</div>

			<div
				class="my-10 flex max-w-full flex-col items-start justify-center gap-8 rounded-3xl bg-gray-800 p-8
					sm:w-[50rem] sm:flex-row sm:justify-start xl:my-20 xl:py-20"
			>
				<div class="flex w-full items-center justify-center sm:w-auto">
					<nav
						class="mb-2 flex items-center justify-start overflow-x-scroll pb-2 sm:flex-col sm:items-start sm:justify-center"
					>
						<button
							class={`flex flex-col items-center justify-center gap-2 bg-white pt-2 duration-500
								ease-in-out sm:flex-row-reverse sm:pt-0 ${styles[0] ? 'bg-opacity-5' : 'bg-opacity-0'}`}
							on:click={() => handleClick(0)}
						>
							<h3
								class={`w-max px-6 duration-500
								ease-in-out ${styles[0] ? 'text-cyan-500' : 'text-neutral-400'}`}
							>
								CU LAIR Lab
							</h3>
							<div
								class={`duration-500ease-in-out h-0.5 w-full  rounded-l-full sm:h-12 sm:w-0.5 
								sm:rounded-t-full ${styles[0] ? 'bg-cyan-500' : 'bg-slate-600'}`}
							/>
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
	</div>
</div>
