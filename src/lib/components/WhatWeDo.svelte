<script lang="ts">
	import { Braces, Cpu, DraftingCompass, Workflow } from '@lucide/svelte';
</script>

<section id="services" aria-labelledby="services-title" class="border-b p-5 md:p-8">
	<div class="mx-auto max-w-6xl space-y-8">
		<div class="max-w-3xl space-y-4">
			<p class="text-sm font-medium text-primary uppercase">Szolgáltatások</p>
			<h2 id="services-title" class="roboto-slab text-2xl font-bold">Amiben segítünk</h2>
			<p class="text-muted-foreground">
				Egyedi szoftveres és gépészeti megoldásokat tervezünk, fejlesztünk és vezetünk be — az első
				ötlettől a működő rendszerig.
			</p>
		</div>

		<div class="grid gap-5 lg:grid-cols-2">
			<article class="card justify-between gap-3 py-4 shadow-xs">
				<header class="gap-0 px-4">
					<div class="flex items-center gap-3">
						<div
							class="flex size-10 shrink-0 items-center justify-center rounded-md border bg-zinc-100 text-primary"
						>
							<Braces class="size-5" aria-hidden="true" />
						</div>
						<h3 class="roboto-slab text-xl font-bold">Szoftverfejlesztés</h3>
					</div>
					<p class="pt-2 text-base text-muted-foreground">
						Webes alkalmazások, admin felületek és üzleti rendszerek stabil, bővíthető alapokon.
					</p>
				</header>

				<div class="flex flex-wrap gap-2 border-t px-4 pt-4">
					<span class="badge">Frontend</span>
					<span class="badge">Backend</span>
					<span class="badge">IoT</span>
				</div>
			</article>

			<article class="card justify-between gap-3 py-4 shadow-xs">
				<header class="gap-0 px-4">
					<div class="flex items-center gap-3">
						<div
							class="flex size-10 shrink-0 items-center justify-center rounded-md border bg-zinc-100 text-primary"
						>
							<Workflow class="size-5" aria-hidden="true" />
						</div>
						<h3 class="roboto-slab text-xl font-bold">Folyamatautomatizálás</h3>
					</div>
					<p class="pt-2 text-base text-muted-foreground">
						Kézi lépések kiváltása, adatkapcsolatok és belső workflow-k összekötése mérhető
						eredménnyel.
					</p>
				</header>

				<div class="flex flex-wrap gap-2 border-t px-4 pt-4">
					<span class="badge">Integráció</span>
					<span class="badge">Dashboard</span>
					<span class="badge">Riport</span>
				</div>
			</article>

			<article class="card justify-between gap-3 py-4 shadow-xs">
				<header class="gap-0 px-4">
					<div class="flex items-center gap-3">
						<div
							class="flex size-10 shrink-0 items-center justify-center rounded-md border bg-zinc-100 text-primary"
						>
							<DraftingCompass class="size-5" aria-hidden="true" />
						</div>
						<h3 class="roboto-slab text-xl font-bold">Gépészeti tervezés</h3>
					</div>
					<p class="pt-2 text-base text-muted-foreground">
						Alkatrészek, szerkezetek és célgépek tervezése gyárthatósági és üzemeltetési
						szempontokkal.
					</p>
				</header>

				<div class="flex flex-wrap gap-2 border-t px-4 pt-4">
					<span class="badge">CAD</span>
					<span class="badge">3D modell</span>
					<span class="badge">Dokumentáció</span>
				</div>
			</article>

			<article class="card justify-between gap-3 py-4 shadow-xs">
				<header class="gap-0 px-4">
					<div class="flex items-center gap-3">
						<div
							class="flex size-10 shrink-0 items-center justify-center rounded-md border bg-zinc-100 text-primary"
						>
							<Cpu class="size-5" aria-hidden="true" />
						</div>
						<h3 class="roboto-slab text-xl font-bold">Prototípus & Validáció</h3>
					</div>
					<p class="pt-2 text-base text-muted-foreground">
						Gyors műszaki döntéstámogatás: koncepció, próbaverzió és visszamérhető tanulságok a
						fejlesztés előtt.
					</p>
				</header>

				<div class="flex flex-wrap gap-2 border-t px-4 pt-4">
					<span class="badge">MVP</span>
					<span class="badge">Tesztelés</span>
					<span class="badge">Tanácsadás</span>
				</div>
			</article>
		</div>
	</div>
</section>
