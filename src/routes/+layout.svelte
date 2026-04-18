<script lang="ts">
	import '../styles/main.css';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href="/favicon.ico?v=3" sizes="any" />
	<link rel="icon" href="/favicon-32x32.png?v=3" sizes="32x32" type="image/png" />
	<link rel="icon" href="/favicon-16x16.png?v=3" sizes="16x16" type="image/png" />
	<link rel="icon" href="/favicon.svg?v=3" sizes="any" type="image/svg+xml" />
	<link rel="shortcut icon" href="/favicon.ico?v=3" />
	<link rel="apple-touch-icon" href="/apple-touch-icon.png?v=3" sizes="180x180" />
	<link rel="manifest" href="/site.webmanifest" />
</svelte:head>
{@render children()}
