<script lang="ts">
	import GitHub from '../Icons/GitHub.svelte';
	import Linkedin from '../Icons/Linkedin.svelte';
	import Instagram from '../Icons/Instagram.svelte';
	import SideBar from './SideBar.svelte';
	import { fade } from 'svelte/transition';
	import { onMount } from 'svelte';

	let showSidebar = false;
	let transition = false;
	let styles = [false, false, false, false, false];

	onMount(() => {
		transition = true;
		styles[0] = true;

		const about = document.getElementById('about');
		const experience = document.getElementById('experience');
		const projects = document.getElementById('projects');
		const skills = document.getElementById('skills');
		const contact = document.getElementById('contact');

		const body = document.body;
		const html = document.documentElement;

		const documentHeight = Math.max(
			body.scrollHeight,
			body.offsetHeight,
			html.clientHeight,
			html.scrollHeight,
			html.offsetHeight
		);

		window.onscroll = (event) => {
			if (about && experience && projects && skills && contact) {
				const sections = [about, experience, projects, skills, contact];

				for (let i = 0; i < sections.length; i++) {
					const rect = sections[i].getBoundingClientRect();

					if (scrollY === 0) {
						styles[0] = true;
					} else if (scrollY >= rect.top + scrollY) {
						styles[i] = true;
						if (i > 0) {
							styles[i - 1] = false;
						}
					} else {
						styles[i] = false;
					}

					if (
						!styles[1] &&
						!styles[2] &&
						!styles[3] &&
						!styles[4] &&
						scrollY < documentHeight - window.innerHeight
					) {
						styles[0] = true;
					} else if (scrollY >= documentHeight - window.innerHeight) {
						styles[4] = true;
						styles[3] = false;
					}
				}
			}
		};
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
					<a
						href="#about"
						class={`cursor-pointer rounded-xl px-4 py-2 text-white duration-300 ease-in-out ${
							styles[0] ? 'bg-teal-500' : 'bg-transparent'
						}`}>About</a
					>
					<a
						href="#experience"
						class={`cursor-pointer rounded-xl px-4 py-2 text-white duration-300 ease-in-out ${
							styles[1] ? 'bg-teal-500' : 'bg-transparent'
						}`}>Experience</a
					>
					<a
						href="#projects"
						class={`cursor-pointer rounded-xl px-4 py-2 text-white duration-300 ease-in-out ${
							styles[2] ? 'bg-teal-500' : 'bg-transparent'
						}`}>Projects</a
					>
					<a
						href="#skills"
						class={`cursor-pointer rounded-xl px-4 py-2 text-white duration-300 ease-in-out ${
							styles[3] ? 'bg-teal-500' : 'bg-transparent'
						}`}>Skills</a
					>
					<a
						href="#contact"
						class={`cursor-pointer rounded-xl px-4 py-2 text-white duration-300 ease-in-out ${
							styles[4] ? 'bg-teal-500' : 'bg-transparent'
						}`}>Contact</a
					>
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
