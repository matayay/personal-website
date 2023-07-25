<script lang="ts">
	import starWarsGif from '../assets/starwars.gif';
	import GitLink from './GitLink.svelte';
	import RepoLink from './RepoLink.svelte';
</script>

<div class="flex w-full items-center justify-center">
	<div class="flex flex-col items-center justify-center gap-6 sm:hidden">
		<div class="flex flex-col items-center justify-center gap-1">
			<div class="flex items-center justify-center gap-4">
				<h1 class="text-xl font-bold text-neutral-400">Star Wars Hub</h1>
				<div class="flex items-center justify-center gap-2">
					<GitLink link="https://github.com/matayay/StarWarsHub" />
					<RepoLink link="https://star-wars-hub.vercel.app/" />
				</div>
			</div>
			<ul class="item-center flex flex-wrap justify-center gap-x-3 gap-y-0">
				<li class="font-mono text-neutral-500">Firebase</li>
				<li class="font-mono text-neutral-500">React</li>
				<li class="font-mono text-neutral-500">Tailwind</li>
				<li class="font-mono text-neutral-500">Typescript</li>
			</ul>
		</div>

		<button
			class="flex items-center justify-center"
			on:click={() => window.open('https://star-wars-hub.vercel.app/')}
		>
			<img
				class="h-auto w-3/4 rounded-lg border-4 border-sky-900"
				src={starWarsGif}
				alt="Project Preview"
			/>
		</button>

		<p class="px-6 text-center font-bold text-neutral-500">
			Star Wars forum that allows users to create, edit, and delete posts. Can also like and comment
			on posts. Post content includes titel, body, and an optional image url.
		</p>
	</div>

	<!-- ################ -->

	<div class="hidden w-11/12 items-center justify-center gap-4 sm:flex xl:w-[70rem]">
		<div class="flex flex-col items-start justify-center gap-4">
			<div class="flex items-center justify-center gap-4">
				<h1 class="text-2xl font-bold text-neutral-400 md:text-3xl">Star Wars Hub</h1>
				<div class="flex items-center justify-center gap-2">
					<GitLink link="https://github.com/matayay/StarWarsHub" />
					<RepoLink link="https://star-wars-hub.vercel.app/" />
				</div>
			</div>

			<p
				class="rounded-lg bg-gray-800 p-6 text-left text-sm font-bold text-neutral-400 lg:text-base"
			>
				Star Wars forum that allows users to create, edit, and delete posts. Can also like and
				comment on posts. Post content includes title, body, and an optional image url.
			</p>

			<ul class="item-center flex flex-wrap justify-center gap-x-3 gap-y-0">
				<li class="font-mono text-neutral-500">Firebase</li>
				<li class="font-mono text-neutral-500">React</li>
				<li class="font-mono text-neutral-500">Tailwind</li>
				<li class="font-mono text-neutral-500">Typescript</li>
			</ul>
		</div>

		<button
			class="flex items-center justify-center"
			on:click={() => window.open('https://star-wars-hub.vercel.app/')}
		>
			<img
				class="h-auto w-full rounded-lg border-4 border-sky-900"
				src={starWarsGif}
				alt="Project Preview"
			/>
		</button>
	</div>
</div>
