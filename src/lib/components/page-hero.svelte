<script lang="ts">
	let {
		title,
		breadcrumbs
	}: {
		title: string;
		breadcrumbs?: Array<{ label: string; href?: string }>;
	} = $props();
</script>

<section class="relative overflow-hidden bg-navy py-24 lg:py-32">
	<div class="gradient-mesh-bg absolute inset-0"></div>

	<svg class="absolute top-12 right-16 h-48 w-48 text-white/[0.03]" style="animation: float 6s ease-in-out infinite;" viewBox="0 0 100 100" fill="none" stroke="currentColor" stroke-width="2">
		<polyline points="30,20 10,50 30,80" />
		<polyline points="40,20 20,50 40,80" />
		<polyline points="60,20 80,50 60,80" />
		<polyline points="70,20 90,50 70,80" />
	</svg>
	<svg class="absolute bottom-8 left-12 h-32 w-32 text-white/[0.03]" style="animation: float-reverse 7s ease-in-out infinite;" viewBox="0 0 100 100" fill="none" stroke="currentColor" stroke-width="2">
		<polyline points="30,20 10,50 30,80" />
		<polyline points="40,20 20,50 40,80" />
		<polyline points="60,20 80,50 60,80" />
		<polyline points="70,20 90,50 70,80" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		{#if breadcrumbs?.length}
			<nav class="mb-6 flex items-center gap-2" aria-label="Breadcrumb">
				{#each breadcrumbs as crumb, i (crumb.label)}
					{#if i > 0}
						<span class="text-xs text-slate">&raquo;</span>
					{/if}
					{#if crumb.href && i < breadcrumbs.length - 1}
						<a
							href={crumb.href}
							class="text-xs font-medium uppercase tracking-widest text-slate transition-colors hover:text-primary"
						>
							{crumb.label}
						</a>
					{:else}
						<span class="text-xs font-medium uppercase tracking-widest text-white">{crumb.label}</span>
					{/if}
				{/each}
			</nav>
		{/if}
		<h1 class="max-w-3xl font-heading text-[clamp(2rem,4vw,3.5rem)] font-bold leading-tight tracking-tight text-white">
			{title}
		</h1>
		<div class="mt-6 h-1 w-16 rounded-full bg-primary"></div>
	</div>
</section>
