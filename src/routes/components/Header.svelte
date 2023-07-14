<script lang="ts">
	import GitHub from './GitHub.svelte';
	import Linkedin from './Linkedin.svelte';
	import Instagram from './Instagram.svelte';
	import Resume from './Resume.svelte';
	import SideBar from './SideBar.svelte';
	import { onMount } from 'svelte';

	let showSidebar = false;
	let transition = false;
	let styles = [false, false, false, false, false];

	onMount(() => {
		styles[0] = true;
		transition = true;

		let body = document.body;
		let html = document.documentElement;

		let documentHeight = Math.max(
			body.scrollHeight,
			body.offsetHeight,
			html.clientHeight,
			html.scrollHeight,
			html.offsetHeight
		);

		window.onresize = (event) => {
			body = document.body;
			html = document.documentElement;

			documentHeight = Math.max(
				body.scrollHeight,
				body.offsetHeight,
				html.clientHeight,
				html.scrollHeight,
				html.offsetHeight
			);
		};

		window.onscroll = (event) => {
			body = document.body;
			html = document.documentElement;

			documentHeight = Math.max(
				body.scrollHeight,
				body.offsetHeight,
				html.clientHeight,
				html.scrollHeight,
				html.offsetHeight
			);

			const about = document.getElementById('about');
			const experience = document.getElementById('experience');
			const projects = document.getElementById('projects');
			const skills = document.getElementById('skills');
			const contact = document.getElementById('contact');

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
						scrollY + 100 < documentHeight - window.innerHeight
					) {
						styles[0] = true;
					} else if (scrollY + 100 >= documentHeight - window.innerHeight) {
						styles[4] = true;
						styles[3] = false;
					} else if (styles[0] || styles[1] || styles[2] || styles[3]) {
						styles[4] = false;
					}
				}
			}
		};
	});
</script>

<div class="sticky left-0 top-0 z-50">
	<header
		class={`flex h-20 items-center justify-end bg-gradient-to-b from-sky-950 px-6 delay-[3500ms] duration-[1500ms] ease-in ${
			transition ? 'opacity-100' : 'opacity-0'
		}`}
	>
		<div class="hidden min-w-full items-center justify-around sm:flex">
			<nav class="flex items-center justify-center lg:gap-8">
				<a
					href="#about"
					class={`cursor-pointer rounded-xl px-2 py-1 text-sm text-white duration-300 ease-in-out md:px-4 md:py-2 lg:text-lg ${
						styles[0] ? 'bg-teal-500' : 'bg-transparent'
					}`}>About</a
				>
				<a
					href="#experience"
					class={`cursor-pointer rounded-xl px-2 py-1 text-sm text-white duration-300 ease-in-out md:px-4 md:py-2 lg:text-lg ${
						styles[1] ? 'bg-teal-500' : 'bg-transparent'
					}`}>Experience</a
				>
				<a
					href="#projects"
					class={`cursor-pointer rounded-xl px-2 py-1 text-sm text-white duration-300 ease-in-out md:px-4 md:py-2 lg:text-lg ${
						styles[2] ? 'bg-teal-500' : 'bg-transparent'
					}`}>Projects</a
				>
				<a
					href="#skills"
					class={`cursor-pointer rounded-xl px-2 py-1 text-sm text-white duration-300 ease-in-out md:px-4 md:py-2 lg:text-lg ${
						styles[3] ? 'bg-teal-500' : 'bg-transparent'
					}`}>Skills</a
				>
				<a
					href="#contact"
					class={`cursor-pointer rounded-xl px-2 py-1 text-sm text-white duration-300 ease-in-out md:px-4 md:py-2 lg:text-lg ${
						styles[4] ? 'bg-teal-500' : 'bg-transparent'
					}`}>Contact</a
				>
			</nav>

			<nav class="flex items-center justify-center gap-1 lg:gap-8">
				<GitHub />
				<Linkedin />
				<Instagram />
				<Resume />
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
