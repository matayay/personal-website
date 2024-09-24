<script lang="ts">
	import checkers from '../assets/checkers.png';
	import GitLink from './GitLink.svelte';
	import RepoLink from './RepoLink.svelte';
</script>

<div class="flex w-full items-center justify-center">
	<div class="flex flex-col items-center justify-center gap-6 sm:hidden">
		<div class="flex flex-col items-center justify-center gap-1">
			<div class="flex items-center justify-center gap-4">
				<h1 class="text-xl font-bold text-neutral-400">Checkers</h1>
				<div class="flex items-center justify-center gap-2">
					<GitLink link="https://github.com/matayay/checkers" />
				</div>
			</div>
			<ul class="item-center flex flex-wrap justify-center gap-x-3 gap-y-0">
				<li class="font-mono text-neutral-500">C++</li>
				<li class="font-mono text-neutral-500">Qt</li>
			</ul>
		</div>

		<div class="flex items-center justify-center">
			<img
				class="h-auto w-3/4 rounded-lg border-4 border-sky-900"
				src={checkers}
				alt="Project Preview"
			/>
		</div>

		<p class="px-6 text-center text-xs font-bold text-neutral-500">
			Standard two player checkers game. Game is played on a 8x8 board with 12 pieces per player.
			May move diagonally and can take enemy by jumping over them. Supports chain jumping. The game
			will end when one player has no more peices, neither player can move, or is ended manually.
			Logic written in C++. Qt Creator used for GUI.
		</p>
	</div>

	<!-- ################ -->

	<div class="hidden w-11/12 items-center justify-center gap-4 sm:flex xl:w-[70rem]">
		<div class="flex items-center justify-center">
			<img
				class="h-auto w-full rounded-lg border-4 border-sky-900"
				src={checkers}
				alt="Project Preview"
			/>
		</div>

		<div class="flex flex-col items-end justify-center gap-4">
			<div class="flex items-center justify-center gap-4">
				<div class="flex items-center justify-center gap-2">
					<GitLink link="https://github.com/matayay/checkers" />
				</div>
				<h1 class="text-2xl font-bold text-neutral-400 md:text-3xl">Checkers</h1>
			</div>

			<p
				class="rounded-lg bg-gray-800 p-6 text-right text-xs font-bold text-neutral-400 lg:text-base"
			>
				Standard two player checkers game. Game is played on a 8x8 board with 12 pieces per player.
				May move diagonally and can take enemy by jumping over them. Supports chain jumping. The
				game will end when one player has no more peices, neither player can move, or is ended
				manually. Logic written in C++. Qt Creator used for GUI.
			</p>

			<ul class="item-center flex flex-wrap justify-center gap-x-3 gap-y-0">
				<li class="font-mono text-neutral-500">C++</li>
				<li class="font-mono text-neutral-500">Qt</li>
			</ul>
		</div>
	</div>
</div>
