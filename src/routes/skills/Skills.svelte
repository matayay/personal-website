<script lang="ts">
	import { inview } from 'svelte-inview';
	import Waves from './components/Waves.svelte';
	let isInView: boolean;
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
			class={`flex min-h-screen flex-col items-center pt-20 duration-1000 ease-in ${
				isInView ? 'opacity-100' : 'opacity-0'
			}`}
			id="skills"
		>
			<div class="flex w-full flex-col items-center justify-center gap-1 lg:gap-4">
				<h2 class="text-center text-2xl text-neutral-300 xl:text-5xl">My Skills</h2>
				<div class="h-1 w-3/4 rounded-3xl bg-gray-800" />
			</div>

			<Waves />
		</section>
	</div>
</div>
