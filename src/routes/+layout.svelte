<script lang="ts">
	import '../app.css';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href="/images/logos/emblem.png" />
	<title>PICPA - Philippine Institute of Certified Public Accountants</title>
</svelte:head>

{@render children()}
