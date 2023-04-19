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
<footer>
	<p>Fjader Media</p>
	<p>Videoita tarinoista ja ihmisistä jotka jäävät mieleen</p>
</footer>
