<script lang="ts">
	import dungeon from '../assets/dungeon.gif';
	import GitLink from './GitLink.svelte';
	import RepoLink from './RepoLink.svelte';
</script>

<div class="flex items-center justify-center">
	<div class="flex flex-col items-center justify-center gap-6 sm:hidden">
		<div class="flex flex-col items-center justify-center gap-1">
			<div class="flex items-center justify-center gap-4">
				<h1 class="text-xl font-bold text-neutral-400">Dungeon Escape</h1>
				<div class="flex items-center justify-center gap-2">
					<GitLink link="https://github.com/matayay/Dungeon-Escape" />
				</div>
			</div>
			<ul class="item-center flex flex-wrap justify-center gap-x-3 gap-y-0">
				<li class="font-mono text-neutral-500">C++</li>
			</ul>
		</div>

		<div class="flex items-center justify-center">
			<img
				class="h-auto w-3/4 rounded-lg border-4 border-sky-900"
				src={dungeon}
				alt="Project Preview"
			/>
		</div>

		<p class="px-6 text-center text-xs font-bold text-neutral-500">
			This project is developing a single player Dungeon Escape game where the user is prompted to
			enter their player name and the names of four NPC party members. The player must then find a
			way to escape the dungeon and kill an evil sorcerer. Along the way they will be able to fight
			monsters, speak to merchants, find treasure, and solve puzzles. The game ends when either a
			loss condition is met or the player leaves through the dungeon exit after defeating the
			sorcerer.
		</p>
	</div>

	<div class="hidden w-11/12 items-center justify-center gap-4 sm:flex xl:w-2/3">
		<div class="flex items-center justify-center">
			<img
				class="h-auto w-full rounded-lg border-4 border-sky-900"
				src={dungeon}
				alt="Project Preview"
			/>
		</div>

		<div class="flex flex-col items-end justify-center gap-4">
			<div class="flex items-center justify-center gap-4">
				<div class="flex items-center justify-center gap-2">
					<GitLink link="https://github.com/matayay/Dungeon-Escape" />
				</div>
				<h1 class="text-2xl font-bold text-neutral-400 md:text-3xl">Dungeon Escape</h1>
			</div>

			<p
				class="rounded-lg bg-gray-800 p-6 text-right text-xs font-bold text-neutral-400 lg:text-base"
			>
				This project is developing a single player Dungeon Escape game where the user is prompted to
				enter their player name and the names of four NPC party members. The player must then find a
				way to escape the dungeon and kill an evil sorcerer. Along the way they will be able to
				fight monsters, speak to merchants, find treasure, and solve puzzles. The game ends when
				either a loss condition is met or the player leaves through the dungeon exit after defeating
				the sorcerer.
			</p>

			<ul class="item-center flex flex-wrap justify-center gap-x-3 gap-y-0">
				<li class="font-mono text-neutral-500">C++</li>
			</ul>
		</div>
	</div>
</div>
