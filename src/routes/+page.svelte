<script lang="ts">
	import Card from '$lib/components/Card.svelte';
	import Button from '$lib/components/Button.svelte';

	let contactEmail = 'matti@example.com';
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
</script>

<section>
	<div class="container px-4 py-12 mx-auto">
		<h2 class="text-2xl mb-6">Videoita tarinoista ja ihmisistä jotka jäävät mieleen</h2>
		<p class="text-lg mb-8">
			Paranna yrityksesi tunnettavuutta, kasvata myyntiäsi tai kouluta ihmisiä tyylikkäiden ja
			ammattimaisten videoiden avulla
		</p>
		<div class="mb-4 flex justify-center">
			<Button href="#showreel">Katso esimerkkejä</Button>
		</div>
		<div class="text-center">
			<a href="mailto:{contactEmail}">Ota yhteyttä</a>
		</div>
	</div>
</section>
<section>
	<div class="container px-4 py-12 mx-auto">
		<h2 class="text-2xl mb-6">Videotuotanto</h2>
		<p>
			Toteutan yrityksille ammattimaisesti kuvattuja videoita eri tarkoituksiin, joiden avulla
			parannat yrityksesi tunnettavuutta, myyntiä ja koulutuksia.
		</p>

		<p>
			Videoiden avulla pystyt näyttämään ja kertomaan tuotteestasi tai yrityksestäsi
			mieleenpainuvalla tavalla.
		</p>
		<p>
			Oli tavoitteesi sitten lisätä myyntiä, parantaa tunnettavuuttasi tai kouluttaa tuote tai
			prosessi, niin video on erinomainen työkalu siihen.
		</p>
	</div>
	<div class="container px-4 py-12 mx-auto">
		<div class="flex gap-4 justify-between">
			{#each products as product}
				<div class="mb-6">
					<Card title={product.title} content={product.content} />
				</div>
			{/each}
		</div>
	</div>
</section>
<section>
	<div class="container px-4 py-12 mx-auto">
		<h2 class="text-2xl mb-6">Showreel</h2>
		<Button href="mailto:{contactEmail}">Ota yhteyttä</Button>
	</div>
</section>
<section>
	<div class="container px-4 py-12 mx-auto">
		<h2 class="text-2xl mb-6">Mies kameran takana</h2>
		<p>
			Olen 20 vuotta videoita ammatikseni tehnyt AV -alan ammattilainen. Olen tuottanut yli 150 eri
			tyyppistä videoita, muutamia kohokohtia löydät showreelistä yläpuolella.
		</p>
		<p>
			Työtäni on löytää haluamasi viestin ydin ja kuvata ja tuottaa siitä siitä video, joka välittää
			haluamasi viestin ja saa katsojan vaikuttuneeksi.
		</p>
	</div>
</section>
<section>
	<div class="container px-4 py-12 mx-auto">
		<h2 class="text-2xl mb-6">Laatua vaivattomasti järkihintaan</h2>
		<div class="flex gap-4 justify-between">
			{#each benefits as benefit}
				<div class="mb-6">
					<Card title={benefit.title} content={benefit.content} />
				</div>
			{/each}
		</div>
	</div>
</section>
<section>
	<div class="container px-4 py-12 mx-auto">
		<h2 class="text-2xl mb-6">Hinnasto</h2>
		<p>Videotuotanto on aina yksilöllistä ja lähtee sinun tarpeestasi.</p>
		<div class="my-4">
			<p>Tyypillisesti asiakkaani ovat valmiitä käyttämään</p>
			<p class="text-lg my-2">1 500 € - 5 000 €</p>
			<p>tuottamiini videoihin.</p>
		</div>
		<p>Hinta varmistuu kun olemme yhdessä määrittäneet tarpeesi, ennen kuin sitoudut mihinkään.</p>
		<div class="my-4">
			<Button href="mailto:{contactEmail}">Ota yhteyttä</Button>
		</div>
	</div>
</section>
