<script lang="ts">
	type Principle = {
		label: string;
		title: string;
		description: string;
	};

	const principles: Principle[] = [
		{
			label: 'Döntés',
			title: 'Átlátható műszaki irány',
			description:
				'Nem csak megvalósítást adunk, hanem érthető indoklást is: miért azt az irányt érdemes választani.'
		},
		{
			label: 'Használat',
			title: 'A napi munkához igazítva',
			description:
				'A megoldás nem önmagáért készül: akkor jó, ha egyszerűbbé teszi a tényleges folyamatokat.'
		},
		{
			label: 'Alapok',
			title: 'Bővíthető rendszerben gondolkodva',
			description:
				'Úgy tervezzük meg az alapokat, hogy később új igényekkel és kapcsolódó rendszerekkel is számolni lehessen.'
		},
		{
			label: 'Eredmény',
			title: 'Kézzelfogható, bevezethető megoldás',
			description:
				'A cél nem egy látványos prototípus, hanem egy érthetően átadható és használatba vehető rendszer.'
		}
	];
</script>

<section id="process" aria-labelledby="process-title" class="border-b bg-zinc-50 p-5 md:p-8">
	<div class="mx-auto max-w-6xl space-y-8">
		<div class="max-w-3xl space-y-4">
			<p class="text-sm font-medium text-primary uppercase">Szemlélet</p>
			<h2 id="process-title" class="roboto-slab text-2xl font-bold">
				Ami miatt hosszú távon is működik
			</h2>
			<p class="text-muted-foreground">
				A folyamat lépésein túl arra figyelünk, hogy a döntések érthetők, a megoldások használhatók,
				az alapok pedig később is továbbépíthetők legyenek.
			</p>
		</div>

		<div class="grid gap-5 md:grid-cols-2 lg:grid-cols-4">
			{#each principles as principle (principle.title)}
				<article class="card justify-between gap-3 py-4 shadow-xs">
					<header class="gap-0 px-4">
						<span class="badge mb-3 w-fit">{principle.label}</span>
						<h3 class="roboto-slab text-xl font-bold">{principle.title}</h3>

						<p class="pt-2 text-base text-muted-foreground">{principle.description}</p>
					</header>
				</article>
			{/each}
		</div>
	</div>
</section>
