<script lang="ts">
	import branch from './branch.png';
	const time = new Date();
</script>

<footer
	class="flex h-20 items-center justify-center gap-4 border-x-0 border-t-[0.1px] border-gray-500 bg-black"
>
	<h3 class="text-gray-500">© {time.getFullYear()} Matayay Karuna</h3>
	<button on:click={() => window.open('https://github.com/matayay/personal-website')}>
		<img src={branch} alt="Github branch" class="h-8 w-8" />
	</button>
</footer>
