<script lang="ts">
	export let showSidebar: boolean;
	import XIcon from './XIcon.svelte';
	import GitHub from './GitHub.svelte';
	import Linkedin from './Linkedin.svelte';
	import Instagram from './Instagram.svelte';
	import Resume from './Resume.svelte';
</script>

<div
	class={`fixed right-0 top-0 h-screen w-3/4 bg-black duration-500 ease-in-out ${
		showSidebar ? 'translate-x-0' : 'translate-x-full'
	}`}
>
	<div class="flex h-full w-full flex-col gap-4 bg-gradient-radial from-sky-950">
		<div class="flex w-full items-center justify-end p-4">
			<button on:click={() => (showSidebar = false)}>
				<XIcon />
			</button>
		</div>
		<div class="flex flex-col items-center justify-center gap-8">
			<nav class="flex flex-col items-end justify-center gap-8">
				<a
					on:click={() => (showSidebar = false)}
					href="#about"
					class="w-40 rounded-xl bg-teal-500 py-2 text-center text-white">About</a
				>
				<a
					on:click={() => (showSidebar = false)}
					href="#experience"
					class="w-40 rounded-xl bg-teal-500 py-2 text-center text-white">Experience</a
				>
				<a
					on:click={() => (showSidebar = false)}
					href="#projects"
					class="w-40 rounded-xl bg-teal-500 py-2 text-center text-white">Projects</a
				>
				<a
					on:click={() => (showSidebar = false)}
					href="#skills"
					class="w-40 rounded-xl bg-teal-500 py-2 text-center text-white">Skills</a
				>
				<a
					on:click={() => (showSidebar = false)}
					href="#contact"
					class="w-40 rounded-xl bg-teal-500 py-2 text-center text-white">Contact</a
				>
			</nav>
			<nav class="flex flex-col items-center justify-center gap-4">
				<div class="flex items-center justify-center gap-4">
					<GitHub />
					<Linkedin />
				</div>
				<Resume />
			</nav>
		</div>
	</div>
</div>
