<script lang="ts">
	import GitHub from './GitHub.svelte';
	import Linkedin from './Linkedin.svelte';
	import Instagram from './Instagram.svelte';
</script>

<div class="sticky left-0 top-0 bg-black">
	<header
		class="flex h-20 items-center justify-around bg-gradient-to-t from-[rgba(255,255,255,0.05)]"
	>
		<nav class="flex items-center justify-center gap-16">
			<h3 class="cursor-pointer text-white">Home</h3>
			<h3 class="cursor-pointer text-white">About</h3>
			<h3 class="cursor-pointer text-white">Experience</h3>
			<h3 class="cursor-pointer text-white">Projects</h3>
			<h3 class="cursor-pointer text-white">Skills</h3>
		</nav>

		<nav class="flex items-center justify-center gap-16">
			<GitHub />
			<Linkedin />
			<Instagram />
		</nav>
	</header>
</div>
