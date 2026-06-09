<script lang="ts">
	import './layout.css';
	import 'basecoat-css/all';
	import '@fontsource-variable/roboto-slab/wght.css';
	import '@fontsource-variable/inter/wght.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<title>Wéber Kft.</title>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children()}
