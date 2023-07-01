<script lang="ts">
	import GitHub from './GitHub.svelte';
	import Linkedin from './Linkedin.svelte';
	import Instagram from './Instagram.svelte';
	import SideBar from './SideBar.svelte';

	let showSidebar = false;
</script>

<div class="sticky left-0 top-0">
	<header class="flex h-20 items-center justify-end bg-gradient-to-b from-sky-950 px-6">
		<div class="hidden min-w-full items-center justify-around sm:flex">
			<nav class="flex items-center justify-center gap-4 lg:gap-10">
				<button class="cursor-pointer text-white">Home</button>
				<button class="cursor-pointer text-white">About</button>
				<button class="cursor-pointer text-white">Experience</button>
				<button class="cursor-pointer text-white">Projects</button>
				<button class="cursor-pointer text-white">Skills</button>
			</nav>

			<nav class="flex items-center justify-center gap-2 lg:gap-8">
				<GitHub />
				<Linkedin />
				<Instagram />
			</nav>
		</div>

		<button
			class="flex min-h-full cursor-pointer flex-col justify-center gap-2 sm:hidden"
			on:click={() => (showSidebar = true)}
		>
			<div class="h-1 w-10 rounded-xl bg-gray-500" />
			<div class="h-1 w-10 rounded-xl bg-gray-500" />
			<div class="h-1 w-10 rounded-xl bg-gray-500" />
		</button>
	</header>
	<SideBar bind:showSidebar />
</div>

<!-- from-[rgba(0,26,73,0.99)] -->
