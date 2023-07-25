<script lang="ts">
	import waldo from '../assets/waldo.gif';
	import GitLink from './GitLink.svelte';
	import RepoLink from './RepoLink.svelte';
</script>

<div class="flex w-full items-center justify-center">
	<div class="flex flex-col items-center justify-center gap-6 sm:hidden">
		<div class="flex flex-col items-center justify-center gap-1">
			<div class="flex items-center justify-center gap-4">
				<h1 class="text-xl font-bold text-neutral-400">Where's Waldo</h1>
				<div class="flex items-center justify-center gap-2">
					<GitLink link="https://github.com/matayay/Waldo" />
					<RepoLink link="https://waldo-six.vercel.app/" />
				</div>
			</div>
			<ul class="item-center flex flex-wrap justify-center gap-x-3 gap-y-0">
				<li class="font-mono text-neutral-500">CSS</li>
				<li class="font-mono text-neutral-500">Firebase</li>
				<li class="font-mono text-neutral-500">React</li>
				<li class="font-mono text-neutral-500">Typescript</li>
			</ul>
		</div>

		<button
			class="flex items-center justify-center"
			on:click={() => window.open('https://waldo-six.vercel.app/')}
		>
			<img
				class="h-auto w-3/4 rounded-lg border-4 border-sky-900"
				src={waldo}
				alt="Project Preview"
			/>
		</button>

		<p class="px-6 text-center font-bold text-neutral-500">
			Where's Waldo photo tagging app. Upon loading page a timer is started and the user must
			identify Waldo, The Wizard, and Odlaw by clicking on their character icons. Once the all
			characters have ben found the timer stops.
		</p>
	</div>

	<!-- ################ -->

	<div class="hidden w-11/12 items-center justify-center gap-4 sm:flex xl:w-[70rem]">
		<div class="flex flex-col items-start justify-center gap-4">
			<div class="flex items-center justify-center gap-4">
				<h1 class="text-2xl font-bold text-neutral-400 md:text-3xl">Where's Waldo</h1>
				<div class="flex items-center justify-center gap-2">
					<GitLink link="https://github.com/matayay/Waldo" />
					<RepoLink link="https://waldo-six.vercel.app/" />
				</div>
			</div>

			<p
				class="rounded-lg bg-gray-800 p-6 text-left text-sm font-bold text-neutral-400 lg:text-base"
			>
				Where's Waldo photo tagging app. Upon loading page a timer is started and the user must
				identify Waldo, The Wizard, and Odlaw by clicking on their character icons. Once the all
				characters have ben found the timer stops.
			</p>

			<ul class="item-center flex flex-wrap justify-center gap-x-3 gap-y-0">
				<li class="font-mono text-neutral-500">CSS</li>
				<li class="font-mono text-neutral-500">Firebase</li>
				<li class="font-mono text-neutral-500">React</li>
				<li class="font-mono text-neutral-500">Typescript</li>
			</ul>
		</div>

		<button
			class="flex items-center justify-center"
			on:click={() => window.open('https://waldo-six.vercel.app/')}
		>
			<img
				class="h-auto w-full rounded-lg border-4 border-sky-900"
				src={waldo}
				alt="Project Preview"
			/>
		</button>
	</div>
</div>
