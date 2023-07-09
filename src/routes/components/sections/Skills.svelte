<script lang="ts">
	import { inview } from 'svelte-inview';
	let isInView: boolean;
</script>

<div
	class="wrapper"
	use:inview={{ unobserveOnEnter: true, rootMargin: '-20%' }}
	on:inview_change={(event) => {
		const { inView, entry, scrollDirection, observer, node } = event.detail;
		isInView = inView;
	}}
>
	<div class="bg-gradient-to-t from-slate-950">
		<section
			class={`flex min-h-screen flex-col items-center pt-20 duration-1000 ease-in ${
				isInView ? 'opacity-100' : 'opacity-0'
			}`}
			id="skills"
		>
			<div class="flex w-full flex-col items-center justify-center gap-4">
				<h2 class="text-center text-2xl text-neutral-300 sm:text-5xl">My Skills</h2>
				<div class="h-1 w-3/4 rounded-3xl bg-gray-400" />
			</div>
		</section>
	</div>
</div>
