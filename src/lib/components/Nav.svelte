<script lang="ts">
	import { resolve } from '$app/paths';
	import Logo from '$lib/components/Logo.svelte';
	import { Dot } from '@lucide/svelte';
</script>

<nav class="border-b px-5 md:px-8">
	<div class="mx-auto flex max-w-6xl items-center justify-between gap-5">
		<a
			class="group flex items-center gap-5 whitespace-nowrap"
			href={resolve('/')}
			aria-label="Wéber Kft. főoldal"
		>
			<Logo />
			<span class="h-8 w-px bg-border" aria-hidden="true"></span>
			<span class="text-lg font-bold text-foreground">
				Wéber <span class="font-light text-muted-foreground">Kft.</span>
			</span>
		</a>

		<div class="hidden gap-5 md:flex">
			<a
				class="flex items-center font-medium whitespace-nowrap underline-offset-2 hover:underline"
				href="#services"
			>
				<Dot class="stroke-primary" />Szolgáltatások
			</a>
			<a
				class="flex items-center font-medium whitespace-nowrap underline-offset-2 hover:underline"
				href="#process"
			>
				<Dot class="stroke-primary" />Szemlélet
			</a>
			<a
				class="flex items-center font-medium whitespace-nowrap underline-offset-2 hover:underline"
				href="#projects"
			>
				<Dot class="stroke-primary" />Projektek
			</a>
			<a
				class="flex items-center font-medium whitespace-nowrap underline-offset-2 hover:underline"
				href="#contact"
			>
				<Dot class="stroke-primary" />Kapcsolat
			</a>
		</div>
	</div>
</nav>
