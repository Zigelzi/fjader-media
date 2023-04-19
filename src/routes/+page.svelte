<script lang="ts">
	import Card from '$lib/components/Card.svelte';
	import { each } from 'svelte/internal';

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
	<div>
		<h2>Videoita tarinoista ja ihmisistä jotka jäävät mieleen</h2>
		<p>
			Paranna yrityksesi tunnettavuutta, kasvata myyntiäsi tai kouluta ihmisiä tyylikkäiden ja
			ammattimaisten videoiden avulla
		</p>
		<a href="#showreel">Katso esimerkkejä</a>
		<a href="mailto:{contactEmail}">Ota yhteyttä</a>
	</div>
</section>
<section>
	<div>
		<h2>Videotuotanto</h2>
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
	<div>
		{#each products as product}
			<Card title={product.title} content={product.content} />
		{/each}
	</div>
</section>
<section>
	<h2>Showreel</h2>
	<a href="mailto:{contactEmail}">Ota yhteyttä</a>
</section>
<section>
	<h2>Laatua vaivattomasti järkihintaan</h2>
	{#each benefits as benefit}
		<Card title={benefit.title} content={benefit.content} />
	{/each}
</section>
<section>
	<h2>Hinnasto</h2>
	<p>Videotuotanto on aina yksilöllistä ja lähtee sinun tarpeestasi.</p>
	<p>Tyypillisesti asiakkaani ovat valmiitä käyttämään:</p>
	<p>1 500 € - 5 000 €</p>
	<p>Hinta varmistuu kun olemme yhdessä määrittäneet tarpeesi, ennen kuin sitoudut mihinkään.</p>
	<a href="mailto:{contactEmail}">Ota yhteyttä</a>
</section>
