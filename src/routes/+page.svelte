<script lang="ts">
	import Card from '$lib/components/Card.svelte';
	import Button from '$lib/components/Button.svelte';
	import careerStories from '$lib/assets/career-stories.jpg?w=400&h=300&webp';
	import videoCamera from '$lib/assets/video-camera.jpg';

	let contactEmail = 'samppa@fjadermedia.fi';
	let isOverlayVisible = false;
	let products = [
		{
			title: 'Uratarinat',
			content:
				'Paranna työntekijämielikuvaasi kertomalle millaista sinun yrityksessäsi on työskennellä potentiaalisille kandidaateille mieleenpainuvilla uratarinoilla.'
		},
		{
			title: 'Kokemusvideot',
			content:
				'Kerro ihmisen kokemuksista ja ajatuksista tunteita herättävällä tavalla kokemusvideon tai haastattelun avulla.'
		},
		{
			title: 'Koulutusvideot',
			content:
				'Säästä kouluttamiseen käyttämääsi aikaa ja paranna niiden laatua helposti ymmärrettävän koulutusvideon avulla.'
		}
	];

	let benefits = [
		{
			title: 'Laatu',
			content:
				'Haluan olla ylpeä jokaisesta tekemästäni videosta. Siksi lupaan että jokainen tuottamani video on tehty laadukkaasti ja yrityksesi brändin mukaisesti.'
		},
		{
			title: 'Vaivattomuus',
			content:
				'Jätetään vauhti ja vaaralliset tilanteet videolle. Toteutan videot vaivattomasti, säästäen sinulta aikaa ja vaivaa jo valmiiksi kiireisessä arjessasi. Sinun ei tarvitse myöskään olla koskaan aikaisemmin toteuttanut videoita yrityksellesi. Ammattitaitoni on käytössäsi alusta loppuun!'
		},
		{
			title: 'Järkihinta',
			content:
				'Videon tuottaminen ei tarvitse olla kallista. Yksi mies kuvaa ja tuottaa videosi, joten myös maksat yhdelle ihmiselle.'
		}
	];

	function displayModal(event: any) {
		isOverlayVisible = !isOverlayVisible;
		console.log('Clicked button!');
	}
</script>

<section>
	<div class="container px-4 lg:px-0 py-12 mx-auto min-h-[75vh] flex flex-wrap justify-between">
		<div class="max-w-2xl md:basis-1/2 md:pr-4">
			<h2 class="text-4xl mb-6 xl:text-5xl">
				Videoita tarinoista ja ihmisistä jotka jäävät mieleen
			</h2>
			<p class="text-lg mb-8">
				Paranna yrityksesi tunnettavuutta, kasvata myyntiäsi tai kouluta ihmisiä tyylikkäiden ja
				ammattimaisten videoiden avulla
			</p>
			<div class="mb-4 flex justify-center">
				<Button on:click={displayModal} isLink={false}>Katso parhaat palat</Button>
			</div>
			<div class="text-center">
				<a href="mailto:{contactEmail}">Ota yhteyttä sähköpostilla</a>
			</div>
		</div>
		<div class="md:basis-1/2 mt-12 md:mt-0">
			<div
				class=" relative before:block before:inset-0 before:absolute before:inset-x-0 before:bg-stone-950/50 before:rounded-lg"
			>
				<img src={videoCamera} class="rounded-lg" alt="" srcset="" />
			</div>
		</div>
	</div>
</section>
<section class="bg-stone-950 text-stone-50">
	<div class="container px-4 py-12 mx-auto">
		<h2 class="text-4xl font-bold mb-6">Videotuotantoa yrityksille</h2>
		<p class="mb-4">
			Toteutan yrityksille ammattimaisesti kuvattuja videoita, joiden avulla parannat yrityksesi
			tunnettavuutta, myyntiä ja koulutuksia.
		</p>

		<p class="mb-4">
			Videoiden avulla pystyt näyttämään ja kertomaan tuotteestasi tai yrityksestäsi
			mieleenpainuvalla tavalla.
		</p>
		<p class="mb-4">
			Oli tavoitteesi sitten lisätä myyntiä, parantaa tunnettavuuttasi tai kouluttaa tuote tai
			prosessi, niin video on erinomainen työkalu siihen.
		</p>
	</div>
	<div class="container px-4 py-12 mx-auto">
		<h2 class="text-4xl font-bold mb-6">Palvelut</h2>
		<div class="flex gap-8 justify-between flex-wrap">
			{#each products as product}
				<Card title={product.title} content={product.content}>
					<img class="max-w-full" src={careerStories} alt="" srcset="" />
				</Card>
			{/each}
		</div>
	</div>
</section>
<section id="showreel">
	<div class="container px-4 py-12 mx-auto">
		<h3>Showreel</h3>
		<h2 class="text-4xl font-bold">Parhaat palat</h2>
		<div style="padding:56.25% 0 0 0;position:relative;" class="my-8">
			<iframe
				src="https://player.vimeo.com/video/814152881?h=9dd80cab10"
				style="position:absolute;top:0;left:0;width:100%;height:100%;"
				frameborder="0"
				allow="autoplay; fullscreen; picture-in-picture"
				allowfullscreen
				title="Video displaying videos produced by Fjader Media"
			/>
		</div>
		<script src="https://player.vimeo.com/api/player.js"></script>
		<Button href="mailto:{contactEmail}">Ota yhteyttä sähköpostilla</Button>
	</div>
</section>
<section>
	<div class="container px-4 my-12 mx-auto">
		<div class="mb-12 text-center">
			<p class="text-7xl font-bold mb-4">20</p>
			<p>vuotta videoalan kokemusta</p>
		</div>
		<div class="mb-12 text-center">
			<p class="text-7xl font-bold mb-4">150+</p>
			<p>tuotettua videota</p>
		</div>
	</div>
</section>
<section class="bg-stone-950 text-stone-50">
	<div class="container px-4 py-12 mx-auto">
		<p class="text-stone-400">Kolme syytä valita Fjäder Media</p>
		<h2 class="text-4xl font-bold mb-6">Laatua vaivattomasti järkihintaan</h2>
		<div class="flex gap-6 justify-between flex-wrap">
			{#each benefits as benefit}
				<Card title={benefit.title} content={benefit.content} />
			{/each}
		</div>
	</div>
</section>
<section>
	<div class="container px-4 py-12 mx-auto">
		<h2 class="text-2xl mb-6">Hinta</h2>
		<p>Videotuotanto on aina yksilöllistä ja lähtee sinun tarpeestasi.</p>
		<div class="my-4">
			<p>Tyypillisesti asiakkaani ovat valmiitä käyttämään</p>
			<p class="text-lg my-2">1 500 € - 5 000 €</p>
			<p>tuottamiini videoihin.</p>
		</div>
		<p>Hinta varmistuu kun olemme yhdessä määrittäneet tarpeesi, ennen kuin sitoudut mihinkään.</p>
		<div class="my-4">
			<Button href="mailto:{contactEmail}">Ota yhteyttä sähköpostilla</Button>
		</div>
	</div>
</section>
{#if isOverlayVisible}
	<div id="overlay" class="fixed inset-0 bg-stone-800/80 text-stone-50 flex flex-col z-10">
		<div class="flex justify-end absolute md:static inset-x-0 z-20">
			<button class="p-4 text-2xl text-bold mr-2" on:click={displayModal}>X</button>
		</div>
		<div class="grow justify-center flex md:my-8">
			<div class="grow relative">
				<iframe
					src="https://player.vimeo.com/video/814152881?h=9dd80cab10"
					style="position:absolute;top:0;left:0;width:100%;height:100%;"
					frameborder="0"
					allow="autoplay; fullscreen; picture-in-picture"
					allowfullscreen
					title="Video displaying videos produced by Fjader Media"
				/>
			</div>
			<script src="https://player.vimeo.com/api/player.js"></script>
		</div>
	</div>
{/if}
