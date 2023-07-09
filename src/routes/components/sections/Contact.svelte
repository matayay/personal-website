<script lang="ts">
	import { inview } from 'svelte-inview';
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
	<div class="bg-gradient-to-b from-slate-950">
		<section
			class={`flex min-h-[50vh] flex-col items-center py-20 duration-1000 ease-in ${
				isInView ? 'opacity-100' : 'opacity-0'
			}`}
			id="contact"
		>
			<div class="flex w-full flex-col items-center justify-center gap-4">
				<h2 class="text-center text-2xl text-neutral-300 sm:text-5xl">Contact Me</h2>
				<div class="h-1 w-3/4 rounded-3xl bg-gray-800" />
			</div>

			<div class="flex h-[40vh] items-center justify-center">
				<div class="flex flex-col items-center justify-center gap-4">
					<h3 class="text-center text-xl font-bold text-slate-300 sm:text-3xl">
						matayaykaruna@gmail.com
					</h3>
					<h3 class="text-center text-xl font-bold text-slate-300 sm:text-3xl">
						(719) - 480 - 1645
					</h3>
				</div>
			</div>
		</section>
	</div>
</div>
