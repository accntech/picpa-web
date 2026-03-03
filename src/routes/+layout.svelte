<script lang="ts">
	import '../app.css';
	import { page } from '$app/state';
	import Navbar from '$lib/components/navbar.svelte';
	import Footer from '$lib/components/footer.svelte';

	let { children } = $props();

	let isHomepage = $derived(page.url.pathname === '/');
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
	<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet" />
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
