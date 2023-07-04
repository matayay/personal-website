<script lang="ts">
	import GitHub from '../Icons/GitHub.svelte';
	import Linkedin from '../Icons/Linkedin.svelte';
	import Instagram from '../Icons/Instagram.svelte';
	import SideBar from './SideBar.svelte';
	import { fade } from 'svelte/transition';
	import { onMount } from 'svelte';

	let showSidebar = false;
	let transition = false;
	onMount(() => {
		transition = true;
	});
</script>

<div class="sticky left-0 top-0">
	{#if transition}
		<header
			in:fade={{ delay: 3500, duration: 1500 }}
			class="flex h-20 items-center justify-end bg-gradient-to-b from-sky-950 px-6"
		>
			<div class="hidden min-w-full items-center justify-around sm:flex">
				<nav class="flex items-center justify-center gap-4 lg:gap-10">
					<button class="cursor-pointer text-white">About</button>
					<button class="cursor-pointer text-white">Experience</button>
					<button class="cursor-pointer text-white">Projects</button>
					<button class="cursor-pointer text-white">Skills</button>
					<button class="cursor-pointer text-white">Contact</button>
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
	{/if}
</div>
