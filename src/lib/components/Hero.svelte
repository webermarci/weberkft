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
				<p class="text-sm font-medium tracking-[0.18em] text-primary uppercase">
					Szoftver • Gépészet • Automatizálás
				</p>
				<h1 id="hero-title" class="roboto-slab max-w-2xl text-4xl font-bold text-balance">
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

		<aside class="hero-process" aria-labelledby="hero-process-title">
			<div class="hero-process__head">
				<div>
					<p class="text-xs font-medium tracking-[0.18em] text-primary uppercase">Közös munka</p>
					<h2 id="hero-process-title" class="roboto-slab mt-1 text-lg font-bold">
						Így épül fel a közös munka
					</h2>
				</div>

				<svg
					class="hero-mark size-20 text-zinc-300"
					viewBox="0 0 96 96"
					fill="none"
					xmlns="http://www.w3.org/2000/svg"
					aria-hidden="true"
				>
					<circle class="hero-mark__glow" cx="48" cy="48" r="34" />
					<path class="hero-mark__guide" d="M18 48H78M48 18V78" />
					<path class="hero-mark__outer" d="M48 14L77 31V65L48 82L19 65V31L48 14Z" />
					<path class="hero-mark__inner" d="M48 29L64 38V58L48 67L32 58V38L48 29Z" />
					<g class="hero-mark__orbit">
						<circle cx="48" cy="14" r="2" />
						<circle cx="77" cy="65" r="2" />
						<circle cx="19" cy="65" r="2" />
					</g>
					<circle class="hero-mark__center" cx="48" cy="48" r="2.5" />
				</svg>
			</div>

			<ol class="hero-process__list">
				{#each processSteps as step (step.number)}
					<li>
						<span>{step.number}</span>
						<div>
							<h3>{step.title}</h3>
							<p>{step.description}</p>
						</div>
					</li>
				{/each}
			</ol>
		</aside>
	</div>
</section>

<style>
	.hero-process {
		border: 1px solid var(--border);
		border-radius: 1rem;
		background: rgb(255 255 255 / 0.72);
		box-shadow: 0 18px 48px rgb(24 24 27 / 0.06);
		padding: 1.1rem;
	}

	.hero-process__head {
		display: flex;
		align-items: flex-start;
		justify-content: space-between;
		gap: 1rem;
		padding-bottom: 1rem;
	}

	.hero-process__list {
		display: grid;
		gap: 0.85rem;
	}

	.hero-process__list li {
		display: grid;
		grid-template-columns: 2rem 1fr;
		gap: 0.8rem;
		padding-top: 0.85rem;
		border-top: 1px solid var(--border);
	}

	.hero-process__list span {
		color: var(--primary);
		font-size: 0.72rem;
		font-weight: 700;
		letter-spacing: 0.12em;
	}

	.hero-process__list h3 {
		font-weight: 700;
		line-height: 1.2;
	}

	.hero-process__list p {
		margin-top: 0.18rem;
		color: var(--muted-foreground);
		font-size: 0.86rem;
		line-height: 1.45;
	}

	.hero-mark__glow {
		animation: hero-breathe 12s ease-in-out infinite;
		fill: color-mix(in oklch, var(--primary) 14%, transparent);
		transform-origin: center;
	}

	.hero-mark__guide {
		stroke: currentColor;
		stroke-dasharray: 1 6;
		stroke-linecap: round;
		stroke-opacity: 0.5;
	}

	.hero-mark__outer,
	.hero-mark__inner {
		vector-effect: non-scaling-stroke;
	}

	.hero-mark__outer {
		animation: hero-emphasis 12s ease-in-out infinite;
		stroke: var(--primary);
		stroke-linejoin: round;
		stroke-width: 1.4;
	}

	.hero-mark__inner {
		stroke: var(--foreground);
		stroke-opacity: 0.48;
	}

	.hero-mark__orbit {
		animation: hero-orbit 18s linear infinite;
		fill: var(--primary);
		filter: drop-shadow(0 0 7px color-mix(in oklch, var(--primary) 48%, transparent));
		transform-box: view-box;
		transform-origin: center;
	}

	.hero-mark__center {
		fill: var(--foreground);
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
