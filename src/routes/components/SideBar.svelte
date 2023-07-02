<script lang="ts">
	export let showSidebar: boolean;
	import XIcon from './XIcon.svelte';
	import GitHub from './GitHub.svelte';
	import Linkedin from './Linkedin.svelte';
	import Instagram from './Instagram.svelte';
</script>

<div
	class={`fixed right-0 top-0 flex min-h-screen w-3/4 flex-col gap-8 bg-sky-200 duration-500 ease-in-out ${
		showSidebar ? 'translate-x-0' : 'translate-x-full'
	}`}
>
	<div class="flex w-full items-center justify-end p-4">
		<button class="text-6xl text-gray-500" on:click={() => (showSidebar = false)}>
			<XIcon />
		</button>
	</div>
	<div class="flex flex-col items-center justify-center gap-8">
		<nav class="flex flex-col items-end justify-center gap-8">
			<button class="w-40 rounded-xl bg-amber-100 py-2 text-center text-black">About</button>
			<button class="w-40 rounded-xl bg-amber-100 py-2 text-center text-black">Experience</button>
			<button class="w-40 rounded-xl bg-amber-100 py-2 text-center text-black">Projects</button>
			<button class="w-40 rounded-xl bg-amber-100 py-2 text-center text-black">Skills</button>
			<button class="w-40 rounded-xl bg-amber-100 py-2 text-center text-black">Contact</button>
		</nav>
		<nav class="flex items-center justify-center gap-4">
			<GitHub />
			<Linkedin />
			<Instagram />
		</nav>
	</div>
</div>
