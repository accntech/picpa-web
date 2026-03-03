<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';

	const boardArchives = [
		{ year: 'FY 2025-2026' },
		{ year: 'FY 2024-2025' },
		{ year: 'FY 2023-2024' },
		{ year: 'FY 2022-2023' },
		{ year: 'FY 2021-2022' },
		{ year: 'FY 2020-2021' },
		{ year: 'FY 2019-2020' },
		{ year: 'FY 2018-2019' },
		{ year: 'FY 2017-2018' }
	];

	const sections = [
		{
			title: 'Chapter Presidents',
			desc: 'Local chapter leaders across 84 chapters nationwide',
			icon: 'M18 18.72a9.094 9.094 0 0 0 3.741-.479 3 3 0 0 0-4.682-2.72m.94 3.198.001.031c0 .225-.012.447-.037.666A11.944 11.944 0 0 1 12 21c-2.17 0-4.207-.576-5.963-1.584A6.062 6.062 0 0 1 6 18.719m12 0a5.971 5.971 0 0 0-.941-3.197m0 0A5.995 5.995 0 0 0 12 12.75a5.995 5.995 0 0 0-5.058 2.772m0 0a3 3 0 0 0-4.681 2.72 8.986 8.986 0 0 0 3.74.477m.94-3.197a5.971 5.971 0 0 0-.94 3.197M15 6.75a3 3 0 1 1-6 0 3 3 0 0 1 6 0Zm6 3a2.25 2.25 0 1 1-4.5 0 2.25 2.25 0 0 1 4.5 0Zm-13.5 0a2.25 2.25 0 1 1-4.5 0 2.25 2.25 0 0 1 4.5 0Z'
		},
		{
			title: 'National Committees',
			desc: 'Specialized committees driving PICPA\'s initiatives and programs',
			icon: 'M3.75 3v11.25A2.25 2.25 0 0 0 6 16.5h2.25M3.75 3h-1.5m1.5 0h16.5m0 0h1.5m-1.5 0v11.25A2.25 2.25 0 0 1 18 16.5h-2.25m-7.5 0h7.5m-7.5 0-1 3m8.5-3 1 3m0 0 .5 1.5m-.5-1.5h-9.5m0 0-.5 1.5m.75-9 3-3 2.148 2.148A12.061 12.061 0 0 1 16.5 7.605'
		},
		{
			title: 'Regional Representatives',
			desc: 'Representatives from 9 regions ensuring nationwide representation',
			icon: 'M15 10.5a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1 1 15 0Z'
		},
		{
			title: 'National Secretariat',
			desc: 'The administrative team managing PICPA\'s day-to-day operations',
			icon: 'M2.25 21h19.5m-18-18v18m10.5-18v18m6-13.5V21M6.75 6.75h.75m-.75 3h.75m-.75 3h.75m3-6h.75m-.75 3h.75m-.75 3h.75M6.75 21v-3.375c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21M3 3h12m-.75 4.5H21m-3.75 3H21m-3.75 3H21'
		}
	];

	let openIndex = $state(0);
</script>

<PageHero
	title="Officers & Administration"
	breadcrumbs={[
		{ label: 'Home', href: '/' },
		{ label: 'About', href: '/about' },
		{ label: 'Officers' }
	]}
/>

<section class="bg-white py-24">
	<div class="mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Leadership</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-dark">
					National Board of Directors
				</h2>
				<p class="mt-2 font-medium text-primary">FY 2025-2026</p>
			</div>
		</ScrollReveal>

		<ScrollReveal delay={100}>
			<div class="relative mt-10 overflow-hidden rounded-2xl shadow-lg">
				<div class="absolute inset-0 bg-linear-to-r from-navy/40 via-transparent to-navy/40 pointer-events-none z-10"></div>
				<div class="absolute inset-0 bg-linear-to-t from-navy/30 via-transparent to-transparent pointer-events-none z-10"></div>
				<img
					src="/images/officers/nbod-2025-2026.webp"
					alt="National Board of Directors FY 2025-2026"
					class="w-full"
				/>
			</div>
		</ScrollReveal>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-4xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Archives</p>
				<h2 class="mt-3 font-heading text-[clamp(1.5rem,2.5vw,2rem)] font-bold text-dark">
					Board Archives
				</h2>
			</div>
		</ScrollReveal>

		<div class="mt-10 space-y-3">
			{#each boardArchives as archive, i (archive.year)}
				<ScrollReveal stagger={i}>
					<div class="overflow-hidden rounded-xl border-l-2 border-primary bg-white shadow-sm">
						<button
							onclick={() => openIndex = openIndex === i ? -1 : i}
							class="flex w-full cursor-pointer items-center justify-between px-6 py-4 text-left font-heading font-medium text-dark transition-colors hover:text-primary"
						>
							{archive.year}
							<svg
								class="h-5 w-5 shrink-0 text-primary transition-transform duration-300"
								class:rotate-90={openIndex === i}
								viewBox="0 0 20 20"
								fill="none"
								stroke="currentColor"
								stroke-width="2.5"
							>
								<polyline points="6,4 14,10 6,16" />
								<polyline points="10,4 18,10 10,16" />
							</svg>
						</button>
						{#if openIndex === i}
							<div class="border-t border-light px-6 pb-4 pt-3 text-body">
								Board of Directors for {archive.year}. View the complete list on the PICPA MELS portal.
							</div>
						{/if}
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="bg-white py-24">
	<div class="mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="max-w-2xl">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Structure</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold leading-tight text-dark">
					Organizational Sections
				</h2>
			</div>
		</ScrollReveal>

		<div class="mt-14 grid grid-cols-1 gap-6 md:grid-cols-2">
			{#each sections as section, i (section.title)}
				<ScrollReveal stagger={i}>
					<div class="group rounded-2xl bg-light p-8 shadow-sm transition-all duration-300 hover:-translate-y-1 hover:shadow-lg">
						<div class="flex h-12 w-12 items-center justify-center rounded-xl bg-primary/10 transition-colors group-hover:bg-primary/15">
							<svg class="h-6 w-6 text-primary" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
								<path stroke-linecap="round" stroke-linejoin="round" d={section.icon} />
							</svg>
						</div>
						<h3 class="mt-5 font-heading text-xl font-bold text-dark">{section.title}</h3>
						<p class="mt-2 leading-relaxed text-body">{section.desc}</p>
						<div class="mt-5 flex items-center gap-1 text-sm font-medium text-primary transition-colors group-hover:text-primary-dark">
							<span>View on MELS Portal</span>
							<svg class="h-4 w-4 transition-transform group-hover:translate-x-0.5" viewBox="0 0 20 20" fill="none" stroke="currentColor" stroke-width="2">
								<polyline points="6,4 14,10 6,16" />
								<polyline points="10,4 18,10 10,16" />
							</svg>
						</div>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>
