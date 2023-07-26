<script lang="ts">
	import dynamo from './technologies/dynamo.png';
	import Firebase from './technologies/firebase.svelte';
	import Git from './technologies/git.svelte';
	import Lambda from './technologies/lambda.svelte';
	import Node from './technologies/node.svelte';
	import Postgres from './technologies/postgres.svelte';
	import supabase from './technologies/supabase.png';
	import websockets from './technologies/websockets.png';
</script>

<div class="flex flex-col items-center justify-center gap-2 sm:gap-8">
	<h3 class="text-xl font-bold text-neutral-400 sm:text-2xl md:text-3xl">Technologies</h3>
	<div class="flex flex-wrap items-center justify-center gap-2 px-4 sm:gap-12">
		<img src={dynamo} alt="Dynamodb logo" class="h-12 w-12" />
		<Firebase />
		<Git />
		<Lambda />
		<Node />
		<Postgres />
		<img src={supabase} alt="Supabase logo" class="h-12 w-12" />
		<img src={websockets} alt="Websocket protocol logo" class="h-12 w-12" />
	</div>
</div>
