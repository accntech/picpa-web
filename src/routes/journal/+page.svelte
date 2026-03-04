<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';

	const focusAreas = [
		{
			icon: 'building',
			title: 'Philippine Accountancy Profession',
			desc: 'Research on the current state, challenges, and future direction of the accountancy profession in the Philippines.'
		},
		{
			icon: 'chart',
			title: 'Financial Reporting Standards',
			desc: 'Analysis and commentary on Philippine Financial Reporting Standards and their application.'
		},
		{
			icon: 'search',
			title: 'Auditing & Assurance',
			desc: 'Studies on auditing practices, methodologies, and quality assurance in the Philippine context.'
		},
		{
			icon: 'document',
			title: 'Taxation & Regulatory Compliance',
			desc: 'Research on Philippine tax regulations, compliance issues, and policy implications.'
		}
	];

	const articles = [
		{
			title: 'The Philippine Accountancy Profession Research Agenda',
			authors: 'PICPA Research Committee',
			year: '2024',
			abstract: 'A comprehensive research agenda outlining priority areas for academic and professional investigation in Philippine accountancy.'
		},
		{
			title: 'Impact of Digital Transformation on Audit Quality',
			authors: 'Various Contributors',
			year: '2023',
			abstract: 'An examination of how emerging technologies are reshaping audit methodologies and their implications for audit quality in the Philippines.'
		},
		{
			title: 'Sustainability Reporting Practices Among Philippine Listed Companies',
			authors: 'PICPA Foundation Research Team',
			year: '2023',
			abstract: 'A study analyzing the current state of sustainability reporting practices among publicly listed companies in the Philippines.'
		}
	];
</script>

<PageHero title="PICPA Journal" breadcrumbs={[{label: 'Home', href: '/'}, {label: 'Journal'}]} />

<section class="bg-white py-24">
	<div class="mx-auto max-w-4xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<h2 class="font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-dark">Official Research Publication</h2>
				<div class="mx-auto mt-6 h-1 w-16 rounded-full bg-primary"></div>
			</div>
		</ScrollReveal>

		<ScrollReveal delay={100}>
			<div class="relative mx-auto mt-10 max-w-3xl px-8 py-6">
				<svg class="absolute top-0 left-0 h-10 w-10 text-primary/20" viewBox="0 0 100 100" fill="none" stroke="currentColor" stroke-width="4">
					<polyline points="40,25 20,50 40,75" />
					<polyline points="55,25 35,50 55,75" />
				</svg>
				<p class="text-center text-[clamp(1.25rem,2.5vw,1.75rem)] leading-relaxed text-dark/80">
					The PICPA Journal is the official research publication of the Philippine Institute of Certified
					Public Accountants. It serves as a platform for scholarly research, professional insights, and
					thought leadership in the field of accountancy.
				</p>
				<svg class="absolute right-0 bottom-0 h-10 w-10 text-primary/20" viewBox="0 0 100 100" fill="none" stroke="currentColor" stroke-width="4">
					<polyline points="45,25 65,50 45,75" />
					<polyline points="60,25 80,50 60,75" />
				</svg>
			</div>
		</ScrollReveal>
	</div>
</section>

<section class="relative overflow-hidden bg-navy py-24">
	<div class="gradient-mesh-bg absolute inset-0"></div>
	<svg class="pointer-events-none absolute bottom-12 left-16 h-48 w-48 text-white/3" style="animation: float-reverse 7s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<h2 class="font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">Research Focus Areas</h2>
			<p class="mt-3 max-w-2xl text-slate">Our journal covers the critical topics shaping the future of Philippine accountancy.</p>
		</ScrollReveal>

		<div class="mt-14 grid grid-cols-1 gap-6 md:grid-cols-2">
			{#each focusAreas as area, i (area.title)}
				<ScrollReveal stagger={i}>
					<div class="glass rounded-2xl p-8 transition-all duration-300 hover:-translate-y-0.5 hover:shadow-[0_0_30px_rgba(24,179,85,0.1)]">
						<div class="flex h-12 w-12 items-center justify-center rounded-xl bg-primary/10">
							{#if area.icon === 'building'}
								<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M3.75 21h16.5M4.5 3h15M5.25 3v18m13.5-18v18M9 6.75h1.5m-1.5 3h1.5m-1.5 3h1.5m3-6H15m-1.5 3H15m-1.5 3H15M9 21v-3.375c0-.621.504-1.125 1.125-1.125h3.75c.621 0 1.125.504 1.125 1.125V21" />
								</svg>
							{:else if area.icon === 'chart'}
								<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M3 13.125C3 12.504 3.504 12 4.125 12h2.25c.621 0 1.125.504 1.125 1.125v6.75C7.5 20.496 6.996 21 6.375 21h-2.25A1.125 1.125 0 013 19.875v-6.75zM9.75 8.625c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125v11.25c0 .621-.504 1.125-1.125 1.125h-2.25a1.125 1.125 0 01-1.125-1.125V8.625zM16.5 4.125c0-.621.504-1.125 1.125-1.125h2.25C20.496 3 21 3.504 21 4.125v15.75c0 .621-.504 1.125-1.125 1.125h-2.25a1.125 1.125 0 01-1.125-1.125V4.125z" />
								</svg>
							{:else if area.icon === 'search'}
								<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" />
								</svg>
							{:else}
								<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M19.5 14.25v-2.625a3.375 3.375 0 00-3.375-3.375h-1.5A1.125 1.125 0 0113.5 7.125v-1.5a3.375 3.375 0 00-3.375-3.375H8.25m0 12.75h7.5m-7.5 3H12M10.5 2.25H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 00-9-9z" />
								</svg>
							{/if}
						</div>
						<h3 class="mt-5 font-heading text-lg font-bold text-white">{area.title}</h3>
						<p class="mt-2 text-sm leading-relaxed text-white/70">{area.desc}</p>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="bg-white py-24">
	<div class="mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<h2 class="font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-dark">Published Articles</h2>
			<p class="mt-3 text-body">Recent research contributions to the PICPA Journal.</p>
		</ScrollReveal>

		<div class="mt-14 space-y-6">
			{#each articles as article, i (article.title)}
				<ScrollReveal stagger={i}>
					<div class="group flex flex-col gap-6 rounded-2xl border border-gray-100 bg-white p-8 shadow-sm transition-all duration-300 hover:shadow-md lg:flex-row">
						<div class="shrink-0 lg:w-28">
							<span class="inline-block rounded-full bg-primary/10 px-3 py-1 text-xs font-medium text-primary">
								{article.year}
							</span>
						</div>
						<div>
							<h3 class="font-heading text-xl font-bold text-dark transition-colors group-hover:text-primary">{article.title}</h3>
							<p class="mt-2 flex items-center gap-2 text-sm text-primary">
								<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M15.75 6a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0zM4.501 20.118a7.5 7.5 0 0114.998 0A17.933 17.933 0 0112 21.75c-2.676 0-5.216-.584-7.499-1.632z" />
								</svg>
								{article.authors}
							</p>
							<p class="mt-3 leading-relaxed text-body">{article.abstract}</p>
						</div>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="relative overflow-hidden bg-navy py-24">
	<div class="gradient-mesh-bg absolute inset-0"></div>
	<svg class="pointer-events-none absolute -top-8 -right-10 h-72 w-72 text-white/3" style="animation: float 6s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-3xl px-4 text-center lg:px-8">
		<ScrollReveal>
			<div class="flex items-center justify-center gap-3">
				<svg class="h-8 w-8 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
					<path stroke-linecap="round" stroke-linejoin="round" d="M12 7.5h1.5m-1.5 3h1.5m-7.5 3h7.5m-7.5 3h7.5m3-9h3.375c.621 0 1.125.504 1.125 1.125V18a2.25 2.25 0 01-2.25 2.25M16.5 7.5V18a2.25 2.25 0 002.25 2.25M16.5 7.5V4.875c0-.621-.504-1.125-1.125-1.125H4.125C3.504 3.75 3 4.254 3 4.875V18a2.25 2.25 0 002.25 2.25h13.5M6 7.5h3v3H6v-3z" />
				</svg>
				<h2 class="font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">Submit Your Research</h2>
			</div>
			<p class="mt-4 text-lg leading-relaxed text-white/70">
				The PICPA Journal welcomes submissions from CPAs, academics, and researchers. All articles
				undergo peer review to ensure quality and relevance.
			</p>
			<div class="mt-8 flex flex-col items-center gap-4 sm:flex-row sm:justify-center">
				<a
					href="mailto:techsolutions@picpa.com.ph"
					class="inline-flex items-center gap-2 rounded-xl bg-primary px-5 py-3 text-sm font-medium text-white sm:px-8 sm:py-3.5 sm:text-base transition-all hover:bg-primary-dark hover:shadow-[0_0_20px_rgba(24,179,85,0.3)]"
				>
					<svg class="h-5 w-5 shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
						<path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75" />
					</svg>
					Contact for Submission Guidelines
				</a>
			</div>
			<p class="mt-4 text-sm text-white/50">techsolutions@picpa.com.ph</p>
		</ScrollReveal>
	</div>
</section>
