<script lang="ts">
	import '../app.css';
	import Header from './components/Header.svelte';
	import Footer from './components/Footer.svelte';
</script>

<div class="bg-black">
	<Header />
	<slot />
	<Footer />
</div>
