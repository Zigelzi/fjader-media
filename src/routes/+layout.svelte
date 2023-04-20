<script>
	import '$lib/styles/app.css';
	import Navigation from '$lib/components/Navigation.svelte';
</script>

<header>
	<Navigation />
</header>
<main>
	<slot />
</main>
<footer class="bg-stone-950 text-stone-50">
	<div class="px-4 py-6 container mx-auto">
		<p class="font-bold mb-2">Fjader Media</p>
		<p class="text-sm">Videoita tarinoista ja ihmisistä jotka jäävät mieleen</p>
	</div>
</footer>
