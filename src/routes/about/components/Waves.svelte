<script lang="ts">
	import { onMount } from 'svelte';

	let transition = false;
	onMount(() => {
		transition = true;
	});
</script>

<div class="relative w-full flex-grow" style="height: undefined">
	<svg
		class="absolute"
		preserveAspectRatio="none"
		id="visual"
		width="100%"
		height="100%"
		viewBox="0 0 900 675"
		xmlns="http://www.w3.org/2000/svg"
		xmlns:xlink="http://www.w3.org/1999/xlink"
		version="1.1"
	>
		<path
			fill-rule="evenodd"
			clip-rule="evenodd"
			d="M0 448.727L50 336.545C100 224.364 200 0 300 0C400 0 500 224.364 600 238.386C700 252.409 800 56.0909 900 14.0227C1000 -28.0455 1100 84.1364 1150 140.227L1200 196.318V617H1150C1100 617 1000 617 900 617C800 617 700 617 600 617C500 617 400 617 300 617C200 617 100 617 50 617H0V448.727Z"
			fill="#111827"
			class={`z-10 delay-[3500ms] duration-[1500ms] ${transition ? 'opacity-100' : 'opacity-0'}`}
		/>
		<path
			fill-rule="evenodd"
			clip-rule="evenodd"
			d="M0 73.496L50 45.0583C100 16.6206 200 -40.2547 300 45.0583C400 130.371 500 357.873 600 357.873C700 357.873 800 130.371 900 45.0583C1000 -40.2547 1100 16.6206 1150 45.0583L1200 73.496V756H1150C1100 756 1000 756 900 756C800 756 700 756 600 756C500 756 400 756 300 756C200 756 100 756 50 756H0V73.496Z"
			fill="#050D1A"
			class={`z-10 delay-[3500ms] duration-[1500ms] ${transition ? 'opacity-100' : 'opacity-0'}`}
		/>
	</svg>
</div>
