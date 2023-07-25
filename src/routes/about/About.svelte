<script lang="ts">
	import { onMount } from 'svelte';
	import me from './assets/me.jpeg';
	import Waves from './components/Waves.svelte';

	let transition = false;
	onMount(() => {
		transition = true;
	});
</script>

<section class="flex h-screen flex-col" id="about">
	<div
		class="flex h-3/4 w-full flex-col items-center justify-center gap-6 sm:flex-row sm:justify-evenly sm:gap-0"
	>
		<div class="flex flex-col-reverse gap-8 sm:flex-col sm:gap-12">
			<div class="flex flex-col gap-2 sm:gap-6">
				<div class="flex gap-4">
					<h2
						class={`font-mono text-lg text-neutral-300 delay-[750ms] duration-500 sm:text-xl lg:text-4xl ${
							transition ? 'opacity-100' : 'opacity-0'
						}`}
					>
						Hello There,
					</h2>
					<h2
						class={`font-mono text-lg text-neutral-300 delay-[1500ms] duration-500 sm:text-xl lg:text-4xl ${
							transition ? 'opacity-100' : 'opacity-0'
						}`}
					>
						I'm
					</h2>
				</div>

				<h1
					class={`font-sans text-3xl text-white delay-[2500ms] duration-500 sm:text-4xl lg:text-7xl ${
						transition ? 'opacity-100' : 'opacity-0'
					}`}
				>
					Matayay Karuna
				</h1>
			</div>
		</div>

		<div
			class={`flex w-64 flex-col items-start justify-center gap-2
				rounded-xl bg-gradient-to-tl from-sky-950 p-4 delay-[3500ms] duration-[1500ms] sm:w-80 
				xl:w-[38rem] xl:gap-10 xl:p-8 ${transition ? 'opacity-100' : 'opacity-0'}`}
		>
			<div class="flex w-full items-center justify-center">
				<img src={me} alt="Matayay" class="h-auto w-16 rounded-full md:w-28 xl:w-44" />
			</div>
			<article class="flex flex-col gap-1 lg:gap-4">
				<h3 class="text-lg text-neutral-300 lg:text-2xl">A little about me</h3>
				<p class="text-sm text-gray-400 sm:text-xs xl:text-xl">
					I'm an aspiring developer and current CS student at CU Boulder. I have a passion for
					learning and am always looking to discover something new. Some of my hobbies outside tech
					are skiing, video games, and long walks in nature.
				</p>
			</article>
		</div>
	</div>
	<Waves />
</section>
