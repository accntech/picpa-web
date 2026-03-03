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

	<svg class="absolute -top-6 -right-10 h-64 w-64 text-white/3" style="animation: float 6s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>
	<svg class="absolute -bottom-4 -left-6 h-48 w-48 text-white/3" style="animation: float-reverse 7s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
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
