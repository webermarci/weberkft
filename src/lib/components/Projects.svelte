<script lang="ts">
	import { fade } from 'svelte/transition';
	import { ArrowRight, ChevronDown } from '@lucide/svelte';

	type Project = {
		title: string;
		category: string;
		description: string;
	};

	const initialProjectCount = 4;

	const projects: Project[] = [
		{
			title: 'Gyártási státusz dashboard',
			category: 'Folyamatautomatizálás',
			description:
				'Rendelésállapotok, határidők és gépterhelés követése egy átlátható, valós idejű felületen, hogy a napi döntések ne táblázatokból és telefonos egyeztetésekből álljanak.'
		},
		{
			title: 'Egyedi ügyfélportál',
			category: 'Szoftverfejlesztés',
			description:
				'Biztonságos webes felület dokumentumok, ajánlatok és státuszinformációk kezelésére, adminisztrációs háttérrendszerrel és egyszerű ügyféloldali hozzáféréssel.'
		},
		{
			title: 'Célgép koncepcióterv',
			category: 'Gépészeti tervezés',
			description:
				'Gyárthatósági szempontok alapján felépített 3D koncepció, fő méretezési döntésekkel, beépítési javaslatokkal és továbbtervezhető műszaki alapokkal.'
		},
		{
			title: 'IoT mérési prototípus',
			category: 'Prototípus & Validáció',
			description:
				'Szenzoradatok gyűjtése, feldolgozása és vizualizálása bővíthető kísérleti rendszerben, hogy a fejlesztési irány mérhető adatok alapján legyen kiválasztható.'
		},
		{
			title: 'Belső ajánlatkezelő',
			category: 'Üzleti rendszer',
			description:
				'Ajánlatok, státuszok és ügyféladatok rendezett kezelése egy belső admin felületen, ahol az utánkövetés és a felelősségi körök is egyértelműek.'
		},
		{
			title: 'Karbantartási nyilvántartó',
			category: 'Folyamatautomatizálás',
			description:
				'Eszközök, feladatok és határidők követése egyszerű, mobilon is használható felületen, hogy a karbantartás tervezhetőbb és visszakereshető legyen.'
		}
	];

	let showAll = $state(false);
	const visibleProjects = $derived(showAll ? projects : projects.slice(0, initialProjectCount));
</script>

<section id="projects" aria-labelledby="projects-title" class="border-b p-5 md:p-8">
	<div class="mx-auto max-w-6xl space-y-8">
		<div class="max-w-3xl space-y-4">
			<p class="text-sm font-medium tracking-widest text-primary uppercase">Projektek</p>
			<h2 id="projects-title" class="roboto-slab text-2xl font-bold">Korábbi munkáinkból</h2>
			<p class="text-muted-foreground">
				Néhány példa arra, milyen jellegű szoftveres, automatizálási és gépészeti feladatokban
				tudunk segíteni az első ötlettől a használható megoldásig.
			</p>
		</div>

		<div id="project-list" class="overflow-hidden rounded-lg border bg-white shadow-xs">
			{#each visibleProjects as project (project.title)}
				<article
					class="grid gap-3 border-b p-5 last:border-b-0 md:grid-cols-[18rem_1fr] md:gap-8 md:p-6"
					transition:fade={{ duration: 140 }}
				>
					<header class="space-y-3">
						<h3 class="roboto-slab text-xl font-bold">{project.title}</h3>
						<span class="badge">{project.category}</span>
					</header>

					<p class="max-w-3xl text-muted-foreground">{project.description}</p>
				</article>
			{/each}
		</div>

		{#if projects.length > initialProjectCount}
			<div class="flex justify-end">
				<button
					type="button"
					class="btn-primary group justify-center"
					aria-expanded={showAll}
					aria-controls="project-list"
					onclick={() => (showAll = !showAll)}
				>
					{showAll ? 'Kevesebb projekt mutatása' : 'Összes projekt megtekintése'}
					{#if showAll}
						<ChevronDown class="size-4 rotate-180 transition-transform" aria-hidden="true" />
					{:else}
						<ArrowRight
							class="size-4 transition-transform group-hover:translate-x-1"
							aria-hidden="true"
						/>
					{/if}
				</button>
			</div>
		{/if}
	</div>
</section>
