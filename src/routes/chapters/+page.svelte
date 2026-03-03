<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';

	const chapterStats = [
		{ value: 84, suffix: '', label: 'Local Chapters', sub: 'across 9 regions' },
		{ value: 17, suffix: '', label: 'International Chapters', sub: 'worldwide' }
	];

	let displayed = $state(chapterStats.map(() => 0));

	function animateCounters() {
		const duration = 2000;
		const start = performance.now();

		function tick(now: number) {
			const elapsed = now - start;
			const progress = Math.min(elapsed / duration, 1);
			const eased = 1 - Math.pow(1 - progress, 3);
			displayed = chapterStats.map((s) => s.value * eased);
			if (progress < 1) requestAnimationFrame(tick);
		}

		requestAnimationFrame(tick);
	}

	function observe(node: HTMLElement) {
		let triggered = false;
		const observer = new IntersectionObserver(
			(entries) => {
				if (entries[0].isIntersecting && !triggered) {
					triggered = true;
					animateCounters();
				}
			},
			{ threshold: 0.2 }
		);
		observer.observe(node);
		return {
			destroy() {
				observer.disconnect();
			}
		};
	}

	const regions = [
		{
			name: 'National Capital Region (NCR)',
			desc: 'Metro Manila and surrounding areas',
			count: 12
		},
		{
			name: 'Region I — Ilocos',
			desc: 'Ilocos Norte, Ilocos Sur, La Union, Pangasinan',
			count: 8
		},
		{
			name: 'Region II — Cagayan Valley',
			desc: 'Cagayan, Isabela, Nueva Vizcaya, Quirino',
			count: 6
		},
		{
			name: 'Region III — Central Luzon',
			desc: 'Bulacan, Pampanga, Tarlac, Nueva Ecija, Zambales',
			count: 10
		},
		{
			name: 'Region IV — CALABARZON & MIMAROPA',
			desc: 'Cavite, Laguna, Batangas, Rizal, Quezon',
			count: 12
		},
		{
			name: 'Region V — Bicol',
			desc: 'Albay, Camarines Sur, Sorsogon, Catanduanes',
			count: 7
		},
		{
			name: 'Visayas (VI, VII, VIII)',
			desc: 'Western, Central, and Eastern Visayas',
			count: 14
		},
		{
			name: 'Mindanao (IX, X, XI, XII)',
			desc: 'Western, Northern, and Southern Mindanao',
			count: 11
		},
		{
			name: 'CARAGA & BARMM',
			desc: 'Caraga Region and Bangsamoro',
			count: 4
		}
	];

	const internationalGroups = [
		{
			title: 'Asia-Pacific',
			locations: ['Singapore', 'Hong Kong', 'Japan', 'Australia', 'Guam', 'Saipan', 'Palau']
		},
		{
			title: 'Middle East',
			locations: ['UAE', 'Saudi Arabia', 'Qatar', 'Bahrain', 'Kuwait', 'Oman']
		},
		{
			title: 'North America',
			locations: ['USA (East Coast)', 'USA (West Coast)', 'USA (Central)', 'Canada']
		}
	];
</script>

<PageHero
	title="Local & International Chapters"
	breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'Chapters' }]}
/>

<section use:observe class="relative overflow-hidden bg-navy py-20">
	<div class="gradient-mesh-bg absolute inset-0"></div>

	<svg class="absolute -top-8 -right-10 h-72 w-72 text-white/3" style="animation: float 8s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>
	<svg class="absolute bottom-8 left-8 h-40 w-40 text-white/3" style="animation: float-reverse 7s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-4xl px-4 lg:px-8">
		<div class="grid grid-cols-1 gap-8 md:grid-cols-2">
			{#each chapterStats as stat, i (stat.label)}
				<div class="glass rounded-2xl p-10 text-center">
					{#if i === 0}
						<svg class="mx-auto h-10 w-10 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
							<path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
							<path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
						</svg>
					{:else}
						<svg class="mx-auto h-10 w-10 text-gold" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
							<path stroke-linecap="round" stroke-linejoin="round" d="M12 21a9.004 9.004 0 008.716-6.747M12 21a9.004 9.004 0 01-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 017.843 4.582M12 3a8.997 8.997 0 00-7.843 4.582m15.686 0A11.953 11.953 0 0112 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0121 12c0 .778-.099 1.533-.284 2.253m0 0A17.919 17.919 0 0112 16.5c-3.162 0-6.133-.815-8.716-2.247m0 0A9.015 9.015 0 013 12c0-1.605.42-3.113 1.157-4.418" />
						</svg>
					{/if}
					<p class="mt-4 font-heading text-[clamp(2.5rem,5vw,3.5rem)] font-bold {i === 0 ? 'text-primary' : 'text-gold'}">
						{Math.round(displayed[i])}{stat.suffix}
					</p>
					<p class="mt-2 font-heading text-lg font-medium text-white">{stat.label}</p>
					<p class="mt-1 text-sm text-slate">{stat.sub}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="relative overflow-hidden bg-white py-24">
	<svg class="absolute -top-6 -left-10 h-64 w-64 text-primary/3" style="animation: float 9s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<h2 class="font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-dark">
				Regional Chapters
			</h2>
			<p class="mt-3 max-w-xl text-lg text-body">
				PICPA chapters organized across 9 regions in the Philippines
			</p>
			<div class="mt-3 h-1 w-12 rounded-full bg-primary"></div>
		</ScrollReveal>

		<div class="mt-14 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each regions as region, i (region.name)}
				<ScrollReveal stagger={i}>
					<div class="group rounded-2xl bg-white p-7 shadow-md ring-1 ring-black/5 transition-all duration-300 hover:-translate-y-1 hover:shadow-xl" style="transition-timing-function: cubic-bezier(0.22, 1, 0.36, 1);">
						<div class="flex items-start gap-4">
							<div class="flex h-10 w-10 shrink-0 items-center justify-center rounded-xl bg-primary/10">
								<svg class="h-5 w-5 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
									<path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
								</svg>
							</div>
							<div class="min-w-0">
								<h3 class="font-heading text-lg font-bold text-dark">{region.name}</h3>
								<p class="mt-1 text-sm text-body">{region.desc}</p>
							</div>
						</div>
						<div class="mt-5 flex items-center gap-2 opacity-70 transition-opacity duration-300 group-hover:opacity-100">
							<svg class="h-4 w-4 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
								<polyline points="13 17 18 12 13 7" />
								<polyline points="6 17 11 12 6 7" />
							</svg>
							<span class="text-sm font-semibold text-primary">{region.count} chapters</span>
						</div>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="relative overflow-hidden bg-navy py-24">
	<div class="gradient-mesh-bg absolute inset-0"></div>

	<svg class="absolute bottom-12 right-8 h-48 w-48 text-white/3" style="animation: float-reverse 8s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<h2 class="font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">
					International Chapters
				</h2>
				<p class="mx-auto mt-3 max-w-xl text-lg text-slate">
					PICPA's global presence connecting Filipino CPAs worldwide
				</p>
				<div class="mx-auto mt-3 h-1 w-12 rounded-full bg-primary"></div>
			</div>
		</ScrollReveal>

		<div class="mt-14 space-y-12">
			{#each internationalGroups as group, gi (group.title)}
				<ScrollReveal stagger={gi}>
					<div>
						<div class="mb-6 flex items-center gap-3">
							{#if group.title === 'Asia-Pacific'}
								<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M12 21a9.004 9.004 0 008.716-6.747M12 21a9.004 9.004 0 01-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 017.843 4.582M12 3a8.997 8.997 0 00-7.843 4.582m15.686 0A11.953 11.953 0 0112 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0121 12c0 .778-.099 1.533-.284 2.253m0 0A17.919 17.919 0 0112 16.5c-3.162 0-6.133-.815-8.716-2.247m0 0A9.015 9.015 0 013 12c0-1.605.42-3.113 1.157-4.418" />
								</svg>
							{:else if group.title === 'Middle East'}
								<svg class="h-6 w-6 text-gold" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M12 3v2.25m6.364.386l-1.591 1.591M21 12h-2.25m-.386 6.364l-1.591-1.591M12 18.75V21m-4.773-4.227l-1.591 1.591M5.25 12H3m4.227-4.773L5.636 5.636M15.75 12a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0z" />
								</svg>
							{:else}
								<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M2.25 21h19.5m-18-18v18m10.5-18v18m6-13.5V21M6.75 6.75h.75m-.75 3h.75m-.75 3h.75m3-6h.75m-.75 3h.75m-.75 3h.75M6.75 21v-3.375c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21M3 3h12m-.75 4.5H21m-3.75 3.75h.008v.008h-.008v-.008zm0 3h.008v.008h-.008v-.008zm0 3h.008v.008h-.008v-.008z" />
								</svg>
							{/if}
							<h3 class="font-heading text-xl font-bold text-white">{group.title}</h3>
						</div>
						<div class="grid grid-cols-2 gap-4 md:grid-cols-4">
							{#each group.locations as location, li (location)}
								<div
									class="glass rounded-xl px-5 py-3.5 text-center text-sm font-medium text-white transition-all duration-300 hover:-translate-y-0.5 hover:bg-white/15"
									style="transition-timing-function: cubic-bezier(0.22, 1, 0.36, 1); animation-delay: {li * 60}ms;"
								>
									<div class="flex items-center justify-center gap-2">
										<svg class="h-3.5 w-3.5 shrink-0 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
											<path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
											<path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
										</svg>
										{location}
									</div>
								</div>
							{/each}
						</div>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>
