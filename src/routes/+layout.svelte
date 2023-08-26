<script>
	import '$lib/styles/app.css';
	import Navigation from '$lib/components/Navigation.svelte';
	import logo_white from '$lib/assets/logo_fjader_media_736x320_white.png';
</script>

<header>
	<Navigation />
</header>
<main>
	<slot />
</main>
<footer class="bg-stone-950 text-stone-50">
	<div class="px-4 py-6 container mx-auto">
		<img src={logo_white} alt="Logo of Fjäder media" class="max-h-[120px] mx-auto mb-8" />
		<p class="text-sm text-center">Videoita tarinoista ja ihmisistä jotka jäävät mieleen</p>
	</div>
</footer>
