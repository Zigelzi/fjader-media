<script lang="ts">
	import samppaIsHero from '$lib/assets/samppa_ystava.jpeg?format=webp';
	let contactEmail = 'samppa@fjadermedia.fi';
</script>

<section>
	<div class="container px-4 py-12 mx-auto">
		<div class="mb-16">
			<h2 class="text-4xl font-bold mb-8">Yhteystiedot</h2>
			<p class="mb-4">Tässä meikäläisen viralliset tiedot.</p>
			<p class="font-bold">Fjäder Media Oy</p>
			<p>3262468-6</p>
			<p>Korennonkuja 7</p>
			<p>01490 Vantaa</p>
			<a href="mailto:{contactEmail}" class="block">{contactEmail}</a>
			<a href="tel:+358505050922" class="block">+358 50 505 0922</a>
		</div>
		<div>
			<h2 class="text-4xl font-bold mb-8">Minusta</h2>
			<div class="space-y-4">
				<p>Moro!</p>
				<p>
					Mä oon Samppa ja rakastan videoiden tekemistä. Työksi kuitenkin kun videoita tekee, pitää
					niiden täyttää jotain muu funktio ku mun mielihyvä. Niiden pitää aina ratkaista joku
					tietty ongelma, jotta ne toimisivat mahdollisimman hyvin.
				</p>
				<p>
					Mä pyrin suunnittelemaan kuvaukset niin että saadaan tuotettua laadukasta tulosta
					mahdollisimman paljon ja mahdollisimman tehokkaasti.
				</p>
				<p>
					Videot on tuonut leivän pöytään jo yli kymmenen vuotta ja kaikki tuo kokemus on
					käytettävissäsi. Ota yhteyttä ja neuvon sinut ilmaiseksi alkuun videoprojekteissasi!
				</p>
			</div>
			<img src={samppaIsHero} class="rounded-lg my-16" alt="Samppa with videocamera" />
		</div>
	</div>
</section>
