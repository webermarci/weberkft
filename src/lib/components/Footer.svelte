<script lang="ts">
	import { resolve } from '$app/paths';
</script>

<footer class="bg-black p-5 text-white md:p-8">
	<div class="mx-auto flex max-w-6xl items-center justify-between gap-3">
		<p class="text-sm text-white/75">© 2026 Wéber Kft. Minden jog fenntartva.</p>
		<a
			class="text-sm font-medium text-white/80 underline-offset-4 transition-colors hover:text-white hover:underline focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-primary"
			href={resolve('/privacy-policy')}
			target="_blank"
			rel="noreferrer"
		>
			Adatkezelési tájékoztató
		</a>
	</div>
</footer>
