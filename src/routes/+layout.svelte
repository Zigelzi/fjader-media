<script>
	import '$lib/styles/app.css';
	import Navigation from '$lib/components/Navigation.svelte';
	import logo_white from '$lib/assets/logo_fjader_media_736x320_white.png';
	import logo from '$lib/assets/logo_fjader_media_736x320.png';
</script>

<svelte:head>
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://fjadermedia.fi" />
	<meta property="og:title" content="Fjäder Media - Videotuotantoa yrityksille" />
	<meta
		property="og:description"
		content="Videoita tarinoista ja ihmisistä jotka jäävät mieleen. Paranna yrityksesi tunnettavuutta, kasvata myyntiäsi tai kouluta ihmisiä tyylikkäiden ja ammattimaisten videoiden avulla"
	/>
	<meta property="og:image" content={logo} />
</svelte:head>

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
