<script>
	import '$lib/styles/app.css';
	import Navigation from '$lib/components/Navigation.svelte';
	import logo_white from '$lib/assets/logo_fjader_media_736x320_white.png';
	import logo from '$lib/assets/logo_fjader_media_19-1x1.png';
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
	<script
		async
		defer
		src="https://cloud.umami.is/script.js"
		data-website-id="190511ee-f596-4a09-8e2a-8be6ae4b3f3f"
	></script>
</svelte:head>

<header>
	<Navigation />
</header>
<main class="min-h-[60vh]">
	<slot />
</main>
<footer class="bg-stone-950 text-stone-50">
	<div class="px-4 py-6 container mx-auto">
		<a href="/">
			<img src={logo_white} alt="Logo of Fjäder Media" class="max-h-[120px] mx-auto mb-8" />
			<p class="sr-only">Etusivu</p>
		</a>
		<p class="text-sm text-center mb-8">Videoita tarinoista ja ihmisistä jotka jäävät mieleen</p>
		<a href="/yhteystiedot" class="text-center block">Yhteystiedot</a>
	</div>
</footer>
