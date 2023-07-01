<script lang="ts">
	import GitHub from './GitHub.svelte';
	import Linkedin from './Linkedin.svelte';
	import Instagram from './Instagram.svelte';
</script>

<div class="sticky left-0 top-0">
	<header class="flex h-20 items-center justify-end bg-gradient-to-b from-sky-950 px-6">
		<div class="hidden min-w-full items-center justify-around sm:flex">
			<nav class="flex items-center justify-center gap-4 lg:gap-10">
				<h3 class="cursor-pointer text-white">Home</h3>
				<h3 class="cursor-pointer text-white">About</h3>
				<h3 class="cursor-pointer text-white">Experience</h3>
				<h3 class="cursor-pointer text-white">Projects</h3>
				<h3 class="cursor-pointer text-white">Skills</h3>
			</nav>

			<nav class="flex items-center justify-center gap-2 lg:gap-8">
				<GitHub />
				<Linkedin />
				<Instagram />
			</nav>
		</div>

		<button class="flex min-h-full cursor-pointer flex-col justify-center gap-2 sm:hidden">
			<div class="h-1 w-10 bg-gray-300" />
			<div class="h-1 w-10 bg-gray-300" />
			<div class="h-1 w-10 bg-gray-300" />
		</button>
	</header>
</div>

<!-- from-[rgba(0,26,73,0.99)] -->
