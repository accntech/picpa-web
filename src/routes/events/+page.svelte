<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';

	const upcomingEvents = [
		{
			date: 'October 14–15, 2025',
			dayRange: '14–15',
			monthYear: 'Oct 2025',
			title: '14th Philippine Professional Summit (PPS14)',
			location: 'Fiesta Pavilion, The Manila Hotel + Online',
			category: 'Summit',
			desc: 'Themed "5IR: Future-Proofing Filipino Professionals for GLOCAL Economic Growth," this national summit empowers Filipino professionals to lead and thrive during the Fifth Industrial Revolution era. Open to all registered professionals.',
			cpdUnits: '15 CPD Units',
			registrationUrl: 'https://pps14.com',
			pricing: 'Face-to-Face: ₱7,200 (early bird) / ₱8,000 (regular) — Virtual: ₱2,000 / ₱2,500'
		},
		{
			date: 'September 24–26, 2025',
			dayRange: '24–26',
			monthYear: 'Sep 2025',
			title: '6th National Summit on Government Procurement',
			location: 'Ilocos Norte Centennial Arena, Laoag City',
			category: 'Summit',
			desc: 'Comprehensive training on RA No. 12009 (New Government Procurement Act), covering strategic procurement planning, modern procurement modes, contract implementation, and digital procurement tools.',
			cpdUnits: '16 CPD Units',
			registrationUrl: 'https://forms.gle/3zobSLVtjkr5rsW76',
			pricing: '₱5,000 (includes 3-day live-out accommodation)'
		}
	];

	const newsHighlights = [
		{
			date: 'May 26–27, 2025',
			title: 'PICPA National Elections 2025 — Official Results',
			desc: 'Election results for the national board and local chapter leadership positions have been announced.',
			link: 'https://picpa.com.ph/picpa-national-elections-2025-official-results/',
			image: 'https://picpa.com.ph/wp-content/uploads/2025/05/28-1280x1249.webp'
		},
		{
			date: 'May 7, 2025',
			title: 'PICPA Recognized at Malacañang Palace',
			desc: "PICPA was honored at a recognition ceremony for its contributions to the Philippines' successful exit from the FATF Grey List.",
			link: 'https://picpa.com.ph/picpa-recognized-at-the-malacanang-palace/',
			image: 'https://picpa.com.ph/wp-content/uploads/2025/05/amlc_v2.webp'
		},
		{
			date: 'February 1, 2025',
			title: 'PICPA Foundation Coffee Table Book Wins Silver at 60th Anvil Awards',
			desc: "The PICPA Foundation's coffee table book was recognized with a Silver Anvil Award at the prestigious 60th Anvil Awards ceremony.",
			link: 'https://picpa.com.ph/picpa-foundation-coffee-table-book-wins-silver-at-60th-anvil-awards/',
			image: 'https://picpa.com.ph/wp-content/uploads/2025/02/PICPA-Foundation-Coffee-Table-Book-Wins-Silver-at-60thAnvil-Awards-150x150.webp'
		}
	];

	const publications = [
		{
			date: 'November 2025',
			title: 'Accounting Times — September 2025 Edition',
			link: 'https://picpa.com.ph/accounting-times-september-2025-edition/',
			image: 'https://picpa.com.ph/wp-content/uploads/2025/11/Accounting-Times-September-2025-Edition.pdf-1280x1810.webp'
		},
		{
			date: 'September 2025',
			title: 'Accounting Times — August 2025 Edition',
			link: 'https://picpa.com.ph/accounting-times-august-2025-edition/',
			image: 'https://picpa.com.ph/wp-content/uploads/2025/09/Accounting-Times-August-2025-Edition_pages-to-jpg-0001.webp'
		},
		{
			date: 'December 2024',
			title: 'Accounting Times — Uniting CPAs Across Borders',
			link: 'https://picpa.com.ph/uniting-cpas-across-borders/',
			image: 'https://picpa.com.ph/wp-content/uploads/2024/12/1stQrt_AT.webp'
		},
		{
			date: 'July 2024',
			title: 'Accounting Times — 2024 Annual Planning Conference',
			link: 'https://picpa.com.ph/accounting-times-2024-annual-planning-conference/',
			image: 'https://picpa.com.ph/wp-content/uploads/2024/07/APC-jpg.webp'
		}
	];

	const recurringEvents = [
		{
			title: 'Annual National Convention',
			frequency: 'Yearly',
			desc: "PICPA's premier event bringing thousands of CPAs together"
		},
		{
			title: 'Regional Conferences',
			frequency: 'Quarterly',
			desc: 'Regional gatherings for knowledge sharing and networking'
		},
		{
			title: 'CPD Seminars & Workshops',
			frequency: 'Monthly',
			desc: 'Continuing professional development programs for members'
		}
	];
</script>

<PageHero
	title="Events & Announcements"
	breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'Events' }]}
/>

<section class="relative overflow-hidden bg-navy py-6">
	<div class="gradient-mesh-bg pointer-events-none absolute inset-0 opacity-40"></div>
	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<div class="glass flex flex-col gap-4 rounded-2xl px-6 py-4 sm:flex-row sm:items-center">
			<svg class="hidden h-6 w-6 shrink-0 text-primary sm:block" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
				<circle cx="12" cy="12" r="10" />
				<path d="M12 16v-4" />
				<path d="M12 8h.01" />
			</svg>
			<p class="text-sm text-white/80">
				For complete event listings and registration, visit the PICPA Events Portal.
			</p>
			<a
				href="https://picpasystem.com.ph/events/"
				target="_blank"
				rel="noopener noreferrer"
				class="inline-flex shrink-0 items-center justify-center gap-2 rounded-lg bg-primary px-5 py-2.5 text-sm font-medium text-white transition-colors hover:bg-primary-dark sm:ml-auto"
			>
				Visit Events Portal
				<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
					<path d="M7 17L17 7M17 7H7M17 7v10" />
				</svg>
			</a>
		</div>
	</div>
</section>

<section class="relative overflow-hidden bg-navy py-24">
	<div class="gradient-mesh-bg pointer-events-none absolute inset-0 opacity-30"></div>
	<svg class="pointer-events-none absolute -top-8 -right-10 h-72 w-72 text-white opacity-[0.03]" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>
	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="flex items-end justify-between">
				<div>
					<span class="inline-flex items-center gap-2 rounded-full bg-primary/10 px-4 py-1.5 text-xs font-medium text-primary">
						<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
							<rect x="3" y="4" width="18" height="18" rx="2" ry="2" />
							<path d="M16 2v4M8 2v4M3 10h18" />
						</svg>
						Upcoming
					</span>
					<h2 class="mt-4 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">
						Featured Events
					</h2>
				</div>
			</div>
		</ScrollReveal>

		<div class="mt-12 space-y-8">
			{#each upcomingEvents as event, i (event.title)}
				<ScrollReveal stagger={i}>
					<div class="glass group relative overflow-hidden rounded-2xl">
						<div class="absolute inset-0 bg-linear-to-r from-primary/5 to-transparent opacity-0 transition-opacity duration-500 group-hover:opacity-100"></div>
						<div class="relative flex flex-col gap-6 p-6 lg:flex-row lg:p-8">
							<div class="shrink-0 lg:w-44">
								<div class="rounded-2xl bg-linear-to-br from-primary to-primary-dark p-5 text-center text-white">
									<div class="font-heading text-3xl font-bold leading-none">{event.dayRange}</div>
									<div class="mt-1 text-sm font-medium text-white/80">{event.monthYear}</div>
								</div>
							</div>
							<div class="flex-1">
								<div class="flex flex-wrap items-center gap-2">
									<span class="rounded-full bg-primary/10 px-3 py-1 text-xs font-medium text-primary">
										{event.category}
									</span>
									<span class="rounded-full bg-gold/10 px-3 py-1 text-xs font-medium text-gold">
										{event.cpdUnits}
									</span>
								</div>
								<h3 class="mt-3 font-heading text-xl font-bold text-white lg:text-2xl">
									{event.title}
								</h3>
								<p class="mt-2 flex items-center gap-2 text-sm text-slate">
									<svg class="h-4 w-4 shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
										<path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z" />
										<circle cx="12" cy="10" r="3" />
									</svg>
									{event.location}
								</p>
								<p class="mt-3 leading-relaxed text-white/70">{event.desc}</p>
								<div class="mt-5 flex flex-wrap items-center gap-4">
									<a
										href={event.registrationUrl}
										target="_blank"
										rel="noopener noreferrer"
										class="inline-flex items-center gap-2 rounded-lg bg-primary px-6 py-2.5 text-sm font-medium text-white transition-all hover:bg-primary-dark hover:gap-3"
									>
										Register Now
										<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
											<path d="M7 17L17 7M17 7H7M17 7v10" />
										</svg>
									</a>
									<span class="text-sm text-white/50">{event.pricing}</span>
								</div>
							</div>
						</div>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="flex items-end justify-between">
				<div>
					<span class="inline-flex items-center gap-2 rounded-full bg-primary/10 px-4 py-1.5 text-xs font-medium text-primary">
						<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
							<path d="M4 22h16a2 2 0 0 0 2-2V4a2 2 0 0 0-2-2H8a2 2 0 0 0-2 2v16a2 2 0 0 1-2 2Zm0 0a2 2 0 0 1-2-2v-9c0-1.1.9-2 2-2h2" />
							<path d="M18 14h-8M15 18h-5" />
						</svg>
						Latest
					</span>
					<h2 class="mt-4 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-dark">
						News & Highlights
					</h2>
				</div>
			</div>
		</ScrollReveal>

		<div class="mt-12 grid grid-cols-1 gap-8 md:grid-cols-3">
			{#each newsHighlights as item, i (item.title)}
				<ScrollReveal stagger={i}>
					<a
						href={item.link}
						target="_blank"
						rel="noopener noreferrer"
						class="group block overflow-hidden rounded-2xl bg-white shadow-sm transition-all duration-300 hover:-translate-y-1 hover:shadow-lg"
					>
						<div class="relative aspect-video overflow-hidden">
							<img
								src={item.image}
								alt={item.title}
								class="h-full w-full object-cover transition-transform duration-500 group-hover:scale-110"
							/>
							<div class="absolute inset-0 bg-linear-to-t from-navy/60 via-transparent to-transparent opacity-0 transition-opacity duration-300 group-hover:opacity-100"></div>
						</div>
						<div class="p-6">
							<span class="inline-block rounded-full bg-primary/10 px-3 py-1 text-xs font-medium text-primary">
								{item.date}
							</span>
							<h3 class="mt-3 font-heading text-lg font-bold text-dark transition-colors group-hover:text-primary">
								{item.title}
							</h3>
							<p class="mt-2 text-sm leading-relaxed text-body">{item.desc}</p>
							<span class="mt-4 inline-flex items-center gap-1 text-sm font-medium text-primary opacity-0 transition-all duration-300 group-hover:gap-2 group-hover:opacity-100">
								Read more
								<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
									<path d="M5 12h14M12 5l7 7-7 7" />
								</svg>
							</span>
						</div>
					</a>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="relative overflow-hidden bg-white py-24">
	<svg class="pointer-events-none absolute bottom-12 left-8 h-40 w-40 text-navy opacity-[0.03]" style="animation: float-reverse 8s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>
	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div>
				<span class="inline-flex items-center gap-2 rounded-full bg-gold/10 px-4 py-1.5 text-xs font-medium text-gold">
					<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
						<path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z" />
						<path d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z" />
					</svg>
					Accounting Times
				</span>
				<h2 class="mt-4 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-dark">
					Publications
				</h2>
				<p class="mt-2 text-body">Latest editions of the PICPA Accounting Times</p>
			</div>
		</ScrollReveal>

		<div class="mt-12 grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-4">
			{#each publications as pub, i (pub.title)}
				<ScrollReveal stagger={i}>
					<a
						href={pub.link}
						target="_blank"
						rel="noopener noreferrer"
						class="group block overflow-hidden rounded-2xl bg-light transition-all duration-300 hover:-translate-y-2 hover:shadow-xl"
					>
						<div class="relative overflow-hidden">
							<div class="aspect-[3/4]">
								<img
									src={pub.image}
									alt={pub.title}
									class="h-full w-full object-cover transition-transform duration-500 group-hover:scale-105"
								/>
							</div>
							<div class="absolute inset-0 rounded-t-2xl border-2 border-transparent transition-colors duration-300 group-hover:border-primary/30"></div>
						</div>
						<div class="p-5">
							<span class="text-xs font-medium text-primary">{pub.date}</span>
							<h3 class="mt-1 text-sm font-bold text-dark transition-colors group-hover:text-primary">
								{pub.title}
							</h3>
						</div>
					</a>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="relative overflow-hidden bg-navy py-24">
	<div class="gradient-mesh-bg pointer-events-none absolute inset-0 opacity-30"></div>
	<svg class="pointer-events-none absolute bottom-8 right-16 h-48 w-48 text-white opacity-[0.03]" style="animation: float 7s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
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
						<path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2" />
						<circle cx="9" cy="7" r="4" />
						<path d="M23 21v-2a4 4 0 0 0-3-3.87M16 3.13a4 4 0 0 1 0 7.75" />
					</svg>
					Annual Programs
				</span>
				<h2 class="mt-4 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">
					Recurring Events
				</h2>
			</div>
		</ScrollReveal>

		<div class="mt-12 grid grid-cols-1 gap-8 md:grid-cols-3">
			{#each recurringEvents as event, i (event.title)}
				<ScrollReveal stagger={i}>
					<div class="glass group rounded-2xl p-8 text-center transition-all duration-300 hover:-translate-y-1">
						{#if event.frequency === 'Yearly'}
							<div class="mx-auto flex h-14 w-14 items-center justify-center rounded-2xl bg-primary/10">
								<svg class="h-7 w-7 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
									<path d="M8 2v4M16 2v4M3 10h18" />
									<rect x="3" y="4" width="18" height="18" rx="2" />
									<path d="M8 14h.01M12 14h.01M16 14h.01M8 18h.01M12 18h.01" />
								</svg>
							</div>
						{:else if event.frequency === 'Quarterly'}
							<div class="mx-auto flex h-14 w-14 items-center justify-center rounded-2xl bg-primary/10">
								<svg class="h-7 w-7 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
									<path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z" />
									<circle cx="12" cy="10" r="3" />
								</svg>
							</div>
						{:else}
							<div class="mx-auto flex h-14 w-14 items-center justify-center rounded-2xl bg-primary/10">
								<svg class="h-7 w-7 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
									<path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z" />
									<path d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z" />
								</svg>
							</div>
						{/if}
						<span class="mt-4 inline-block text-xs font-semibold uppercase tracking-widest text-primary">
							{event.frequency}
						</span>
						<h3 class="mt-3 font-heading text-lg font-bold text-white">
							{event.title}
						</h3>
						<p class="mt-2 text-sm leading-relaxed text-white/60">{event.desc}</p>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>
