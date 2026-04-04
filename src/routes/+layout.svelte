<script lang="ts">
	import "$lib/assets/globals.css";

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" type="image/webp" href="/favicon.webp">

	<title>Haruto Nakamura</title>
</svelte:head>

{@render children()}
