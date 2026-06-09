<script lang="ts">
	import { ArrowRight } from '@lucide/svelte';

	const processSteps = [
		{
			number: '1.',
			title: 'Felmérés',
			description: 'Megértjük a célt, a jelenlegi folyamatot és a műszaki környezetet.'
		},
		{
			number: '2.',
			title: 'Koncepció',
			description: 'Letisztázzuk a megoldási irányt, a döntési pontokat és az ütemezést.'
		},
		{
			number: '3.',
			title: 'Megvalósítás',
			description: 'Iteratívan építünk: tervezés, fejlesztés, visszajelzés, finomhangolás.'
		},
		{
			number: '4.',
			title: 'Átadás',
			description: 'Dokumentált, használható rendszert adunk át bevezetéssel és támogatással.'
		}
	];
</script>

<section aria-labelledby="hero-title" class="border-b bg-zinc-50 p-5 md:p-8">
	<div class="mx-auto grid max-w-6xl gap-10 lg:grid-cols-[1fr_22rem] lg:items-center">
		<div class="max-w-3xl space-y-7">
			<div class="space-y-5">
				<p class="text-sm font-medium tracking-widest text-primary uppercase">
					Szoftver • Gépészet • Automatizálás
				</p>
				<h1
					id="hero-title"
					class="roboto-slab max-w-2xl text-4xl font-bold text-balance lg:text-5xl"
				>
					Egyedi mérnöki és szoftveres rendszerek üzleti folyamatokra szabva.
				</h1>
				<p class="max-w-2xl text-muted-foreground">
					Belső alkalmazásokat, automatizált folyamatokat és gépészeti koncepciókat tervezünk
					átlátható műszaki döntésekkel — az első felméréstől a bevezetésig.
				</p>
			</div>

			<div class="flex flex-col gap-3 sm:flex-row">
				<a class="btn-primary group justify-center" href="#contact">
					Beszéljünk róla
					<ArrowRight
						class="size-4 transition-transform group-hover:translate-x-1"
						aria-hidden="true"
					/>
				</a>
				<a class="btn-outline justify-center" href="#projects">Korábbi munkáink</a>
			</div>
		</div>

		<aside
			class="rounded-2xl border bg-white/75 p-4 shadow-xs"
			aria-labelledby="hero-process-title"
		>
			<div class="flex items-start justify-between gap-4 pb-4">
				<div>
					<p class="mb-3 text-xs font-medium tracking-widest text-primary uppercase">Közös munka</p>
					<h2 id="hero-process-title" class="roboto-slab mt-1 text-xl font-bold">
						Így épül fel a közös munka
					</h2>
				</div>

				<svg
					class="size-20 text-zinc-300"
					viewBox="0 0 96 96"
					fill="none"
					xmlns="http://www.w3.org/2000/svg"
					aria-hidden="true"
				>
					<circle class="hero-mark__glow origin-center fill-primary/15" cx="48" cy="48" r="34" />
					<path
						class="stroke-current/50"
						stroke-dasharray="1 6"
						stroke-linecap="round"
						d="M18 48H78M48 18V78"
					/>
					<path
						class="hero-mark__outer stroke-primary"
						stroke-linejoin="round"
						stroke-width="1.5"
						vector-effect="non-scaling-stroke"
						d="M48 14L77 31V65L48 82L19 65V31L48 14Z"
					/>
					<path
						class="stroke-foreground/50"
						vector-effect="non-scaling-stroke"
						d="M48 29L64 38V58L48 67L32 58V38L48 29Z"
					/>
					<g class="hero-mark__orbit origin-center fill-primary drop-shadow-md transform-view">
						<circle cx="48" cy="14" r="2" />
						<circle cx="77" cy="65" r="2" />
						<circle cx="19" cy="65" r="2" />
					</g>
					<circle class="fill-foreground" cx="48" cy="48" r="2.5" />
				</svg>
			</div>

			<ol class="grid gap-3.5">
				{#each processSteps as step (step.number)}
					<li class="flex gap-3 border-t pt-3.5">
						<span class="w-8 shrink-0 self-center text-xs font-bold tracking-widest text-primary">
							{step.number}
						</span>
						<div>
							<h3 class="leading-tight font-bold">{step.title}</h3>
							<p class="mt-1 text-sm leading-normal text-muted-foreground">{step.description}</p>
						</div>
					</li>
				{/each}
			</ol>
		</aside>
	</div>
</section>

<style>
	.hero-mark__glow {
		animation: hero-breathe 12s ease-in-out infinite;
	}

	.hero-mark__outer {
		animation: hero-emphasis 12s ease-in-out infinite;
	}

	.hero-mark__orbit {
		animation: hero-orbit 18s linear infinite;
	}

	@keyframes hero-breathe {
		0%,
		100% {
			opacity: 0.68;
			transform: scale(0.985);
		}
		50% {
			opacity: 1;
			transform: scale(1.015);
		}
	}

	@keyframes hero-emphasis {
		0%,
		100% {
			stroke-opacity: 0.78;
		}
		50% {
			stroke-opacity: 1;
		}
	}

	@keyframes hero-orbit {
		to {
			transform: rotate(360deg);
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.hero-mark__glow,
		.hero-mark__outer,
		.hero-mark__orbit {
			animation: none;
		}
	}
</style>
