<script lang="ts">
	import favicon from '#lib/assets/favicon.png';
	import ogp_image from '#lib/assets/ogp.png';
	import type { LayoutProps } from './$types';

	let { children }: LayoutProps = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	
	<meta property="og:image" content={ogp_image} />
	<meta property="og:site_name" content="Haruto のポートフォリオ" />
	<meta property="og:title" content="Haruto Nakamura" />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://harun-gh.github.io/" />
	<meta property="og:description" content="新大学1年生 / Zig大好き。時代遅れな手書きプログラマー" />
	<meta name="twitter:card" content="summary_large_image" />
	
	<title>Haruto Nakamura</title>
</svelte:head>

<main>
	{@render children()}
</main>
