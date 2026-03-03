<script lang="ts">
	let {
		title,
		breadcrumbs
	}: {
		title: string;
		breadcrumbs?: Array<{ label: string; href?: string }>;
	} = $props();
</script>

<section class="relative overflow-hidden bg-gradient-to-r from-primary-deep to-primary-dark py-20 lg:py-28">
	<div class="absolute inset-0 flex items-center justify-center opacity-5">
		<img src="/images/logos/emblem.png" alt="" class="h-96 w-96 object-contain" />
	</div>

	<div class="relative mx-auto max-w-7xl px-4 text-center lg:px-8">
		<h1 class="font-heading text-4xl font-bold text-white lg:text-5xl">
			{title}
		</h1>

		{#if breadcrumbs?.length}
			<nav class="mt-6 flex items-center justify-center gap-2" aria-label="Breadcrumb">
				{#each breadcrumbs as crumb, i (crumb.label)}
					{#if i > 0}
						<span class="text-sm text-white/50">/</span>
					{/if}
					{#if crumb.href && i < breadcrumbs.length - 1}
						<a
							href={crumb.href}
							class="text-sm text-white/70 transition-colors hover:text-primary"
						>
							{crumb.label}
						</a>
					{:else}
						<span class="text-sm text-white">{crumb.label}</span>
					{/if}
				{/each}
			</nav>
		{/if}
	</div>
</section>
