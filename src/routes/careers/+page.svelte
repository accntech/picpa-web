<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';
</script>

<PageHero
	title="Careers"
	breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'Careers' }]}
/>

<section class="relative overflow-hidden bg-navy py-6">
	<div class="gradient-mesh-bg pointer-events-none absolute inset-0 opacity-40"></div>
	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<div class="glass flex flex-col gap-3 rounded-2xl px-6 py-4 sm:flex-row sm:items-center sm:gap-4">
			<svg class="hidden h-6 w-6 shrink-0 text-primary sm:block" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
				<path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2" />
				<circle cx="9" cy="7" r="4" />
				<path d="M22 21v-2a4 4 0 0 0-3-3.87M16 3.13a4 4 0 0 1 0 7.75" />
			</svg>
			<p class="text-sm text-white/80">
				PICPA offers a free job posting service for accountancy-related positions. Listings are
				active for one month.
			</p>
		</div>
	</div>
</section>

<section class="bg-white py-24">
	<div class="mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div>
				<span class="inline-flex items-center gap-2 rounded-full bg-primary/10 px-4 py-1.5 text-xs font-medium text-primary">
					<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
						<rect x="2" y="7" width="20" height="14" rx="2" ry="2" />
						<path d="M16 21V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v16" />
					</svg>
					Opportunities
				</span>
				<h2 class="mt-4 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-dark">
					Current Job Openings
				</h2>
			</div>
		</ScrollReveal>

		<div class="mt-12 space-y-6">
			<ScrollReveal>
				<div class="group overflow-hidden rounded-2xl border-l-4 border-primary bg-white shadow-sm transition-all duration-300 hover:-translate-y-1 hover:shadow-lg">
					<div class="flex flex-col items-start gap-6 p-6 lg:flex-row lg:p-8">
						<img
							src="/images/careers/hiring-poster.jpg"
							alt="Financial Analyst hiring poster"
							class="w-full shrink-0 rounded-xl object-cover lg:w-48"
						/>
						<div class="flex-1">
							<div class="flex flex-wrap items-center gap-2">
								<span class="inline-flex items-center gap-1.5 rounded-full bg-primary/10 px-3 py-1 text-xs font-medium text-primary">
									<span class="h-1.5 w-1.5 rounded-full bg-primary"></span>
									Active
								</span>
							</div>
							<h3 class="mt-3 font-heading text-xl font-bold text-dark lg:text-2xl">
								Financial Analyst
							</h3>
							<p class="mt-1 font-medium text-body">Asian Hospital and Medical Center</p>
							<p class="mt-2 flex items-center gap-2 text-sm text-body">
								<svg class="h-4 w-4 shrink-0 text-slate" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
									<path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z" />
									<circle cx="12" cy="10" r="3" />
								</svg>
								Muntinlupa City, Metro Manila
							</p>
							<div class="mt-4 flex flex-wrap gap-2">
								<span class="rounded-full border border-dark/10 px-3 py-1 text-xs text-body">
									Full-time
								</span>
								<span class="rounded-full border border-dark/10 px-3 py-1 text-xs text-body">
									Finance
								</span>
								<span class="rounded-full border border-dark/10 px-3 py-1 text-xs text-body">
									Entry-level
								</span>
							</div>
						</div>
					</div>
				</div>
			</ScrollReveal>
		</div>
	</div>
</section>

<section class="relative overflow-hidden bg-navy py-24">
	<div class="gradient-mesh-bg pointer-events-none absolute inset-0 opacity-30"></div>
	<svg class="pointer-events-none absolute top-16 right-12 h-48 w-48 text-white opacity-[0.03]" style="animation: float 6s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>
	<svg class="pointer-events-none absolute bottom-12 left-8 h-32 w-32 text-white opacity-[0.03]" style="animation: float-reverse 7s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<span class="inline-flex items-center gap-2 rounded-full bg-primary/10 px-4 py-1.5 text-xs font-medium text-primary">
					<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
						<path d="M22 10v6M2 10l10-5 10 5-10 5z" />
						<path d="M6 12v5c3 3 9 3 12 0v-5" />
					</svg>
					Growth
				</span>
				<h2 class="mt-4 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">
					Career Development Resources
				</h2>
			</div>
		</ScrollReveal>

		<div class="mt-12 grid grid-cols-1 gap-8 md:grid-cols-3">
			<ScrollReveal class="h-full" stagger={0}>
				<div class="glass group h-full rounded-2xl p-8 text-center transition-all duration-300 hover:-translate-y-1">
					<div class="mx-auto flex h-14 w-14 items-center justify-center rounded-2xl bg-primary/10">
						<svg class="h-7 w-7 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
							<path d="M22 10v6M2 10l10-5 10 5-10 5z" />
							<path d="M6 12v5c3 3 9 3 12 0v-5" />
						</svg>
					</div>
					<h3 class="mt-5 font-heading text-lg font-bold text-white">Becoming a CPA</h3>
					<p class="mt-3 text-sm leading-relaxed text-white/60">
						Learn about the steps to becoming a licensed Certified Public Accountant in the
						Philippines, including education requirements and the CPA board exam.
					</p>
				</div>
			</ScrollReveal>

			<ScrollReveal class="h-full" stagger={1}>
				<div class="glass group h-full rounded-2xl p-8 text-center transition-all duration-300 hover:-translate-y-1">
					<div class="mx-auto flex h-14 w-14 items-center justify-center rounded-2xl bg-primary/10">
						<svg class="h-7 w-7 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
							<circle cx="12" cy="12" r="10" />
							<path d="M2 12h20M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z" />
						</svg>
					</div>
					<h3 class="mt-5 font-heading text-lg font-bold text-white">ASEAN CPA</h3>
					<p class="mt-3 text-sm leading-relaxed text-white/60">
						Explore the ASEAN Mutual Recognition Arrangement that allows CPAs to practice
						across ASEAN member states.
					</p>
				</div>
			</ScrollReveal>

			<ScrollReveal class="h-full" stagger={2}>
				<div class="glass group h-full rounded-2xl p-8 text-center transition-all duration-300 hover:-translate-y-1">
					<div class="mx-auto flex h-14 w-14 items-center justify-center rounded-2xl bg-primary/10">
						<svg class="h-7 w-7 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
							<path d="M9 5H7a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2V7a2 2 0 0 0-2-2h-2" />
							<rect x="9" y="3" width="6" height="4" rx="1" />
							<path d="M9 14l2 2 4-4" />
						</svg>
					</div>
					<h3 class="mt-5 font-heading text-lg font-bold text-white">CIA Challenge</h3>
					<p class="mt-3 text-sm leading-relaxed text-white/60">
						Information about the Certified Internal Auditor certification and how Philippine
						CPAs can pursue this international credential.
					</p>
				</div>
			</ScrollReveal>
		</div>
	</div>
</section>

<section class="relative overflow-hidden bg-navy-mid py-20">
	<div class="gradient-mesh-bg pointer-events-none absolute inset-0"></div>
	<div class="relative mx-auto max-w-4xl px-4 text-center lg:px-8">
		<ScrollReveal>
			<div class="glass rounded-2xl p-6 sm:p-12">
				<div class="mx-auto flex h-16 w-16 items-center justify-center rounded-2xl bg-primary/10">
					<svg class="h-8 w-8 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
						<path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z" />
						<polyline points="22,6 12,13 2,6" />
					</svg>
				</div>
				<h2 class="mt-6 font-heading text-[clamp(1.5rem,3vw,2rem)] font-bold text-white">
					Want to Post a Job?
				</h2>
				<p class="mt-3 text-white/70">
					PICPA members and organizations can post accountancy-related job openings for free.
				</p>
				<a
					href="mailto:membership@picpa.com.ph"
					class="mt-6 inline-flex items-center gap-2 rounded-lg bg-primary px-4 py-3 font-medium text-white text-sm sm:text-base sm:px-6 transition-all hover:bg-primary-dark hover:gap-3"
				>
					<svg class="h-5 w-5 shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
						<path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z" />
						<polyline points="22,6 12,13 2,6" />
					</svg>
					membership@picpa.com.ph
				</a>
			</div>
		</ScrollReveal>
	</div>
</section>
