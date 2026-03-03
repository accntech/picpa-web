<script lang="ts">
	import '../app.css';
	import { page } from '$app/state';
	import Navbar from '$lib/components/Navbar.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();

	let isHomepage = $derived(page.url.pathname === '/');
</script>

<svelte:head>
	<link rel="icon" href="/images/logos/emblem.png" />
	<title>PICPA - Philippine Institute of Certified Public Accountants</title>
</svelte:head>

<div class="font-body text-body">
	<Navbar transparent={isHomepage} />
	<main>
		{@render children()}
	</main>
	<Footer />
</div>
