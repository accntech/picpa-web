<script lang="ts">
	import PageHero from '$lib/components/PageHero.svelte';

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

<PageHero title="Events & Announcements" breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'Events' }]} />

<section class="bg-primary/5 py-8">
	<div class="mx-auto flex max-w-7xl items-center gap-4 px-4">
		<svg class="h-6 w-6 shrink-0 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
			<circle cx="12" cy="12" r="10" />
			<line x1="12" y1="16" x2="12" y2="12" />
			<line x1="12" y1="8" x2="12.01" y2="8" />
		</svg>
		<p class="text-body">
			For complete event listings and registration, visit the PICPA Events Portal.
		</p>
		<a
			href="https://picpasystem.com.ph/events/"
			target="_blank"
			rel="noopener noreferrer"
			class="ml-auto shrink-0 rounded-lg bg-primary px-4 py-2 text-sm font-medium text-white transition hover:bg-primary-dark"
		>
			Visit Events Portal
		</a>
	</div>
</section>

<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="font-heading text-2xl font-bold text-dark">Upcoming Events</h2>
		<div class="mt-8 space-y-6">
			{#each upcomingEvents as event (event.title)}
				<div class="flex flex-col gap-6 rounded-xl bg-light p-6 lg:flex-row">
					<div class="shrink-0 lg:w-40">
						<div class="rounded-xl bg-primary p-4 text-center text-white">
							<div class="text-2xl font-bold">{event.dayRange}</div>
							<div class="text-sm">{event.monthYear}</div>
						</div>
					</div>
					<div class="flex-1">
						<div class="flex flex-wrap items-center gap-2">
							<span class="inline-block rounded-full bg-primary/10 px-3 py-1 text-xs font-medium text-primary">
								{event.category}
							</span>
							<span class="inline-block rounded-full bg-accent/10 px-3 py-1 text-xs font-medium text-accent">
								{event.cpdUnits}
							</span>
						</div>
						<h3 class="mt-2 font-heading text-xl font-bold text-dark">{event.title}</h3>
						<p class="mt-1 flex items-center gap-1 text-sm text-body">
							<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
								<path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z" />
								<circle cx="12" cy="10" r="3" />
							</svg>
							{event.location}
						</p>
						<p class="mt-2 text-body">{event.desc}</p>
						<div class="mt-4 flex flex-wrap items-center gap-4">
							<a
								href={event.registrationUrl}
								target="_blank"
								rel="noopener noreferrer"
								class="inline-flex items-center gap-2 rounded-lg bg-primary px-5 py-2.5 text-sm font-medium text-white transition hover:bg-primary-dark"
							>
								Register Now
								<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
									<path d="M7 17L17 7M17 7H7M17 7v10" />
								</svg>
							</a>
							<span class="text-sm text-body">{event.pricing}</span>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="font-heading text-2xl font-bold text-dark">News & Highlights</h2>
		<div class="mt-8 grid grid-cols-1 gap-6 md:grid-cols-3">
			{#each newsHighlights as item (item.title)}
				<a
					href={item.link}
					target="_blank"
					rel="noopener noreferrer"
					class="group overflow-hidden rounded-xl bg-white transition hover:shadow-lg"
				>
					<div class="aspect-video overflow-hidden bg-gray-100">
						<img
							src={item.image}
							alt={item.title}
							class="h-full w-full object-cover transition group-hover:scale-105"
						/>
					</div>
					<div class="p-5">
						<span class="text-xs font-medium text-primary">{item.date}</span>
						<h3 class="mt-1 font-heading text-lg font-bold text-dark group-hover:text-primary transition">
							{item.title}
						</h3>
						<p class="mt-2 text-sm text-body">{item.desc}</p>
					</div>
				</a>
			{/each}
		</div>
	</div>
</section>

<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="font-heading text-2xl font-bold text-dark">Publications</h2>
		<p class="mt-2 text-body">Latest editions of the PICPA Accounting Times</p>
		<div class="mt-8 grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-4">
			{#each publications as pub (pub.title)}
				<a
					href={pub.link}
					target="_blank"
					rel="noopener noreferrer"
					class="group overflow-hidden rounded-xl bg-light transition hover:shadow-lg"
				>
					<div class="aspect-[3/4] overflow-hidden bg-gray-100">
						<img
							src={pub.image}
							alt={pub.title}
							class="h-full w-full object-cover transition group-hover:scale-105"
						/>
					</div>
					<div class="p-4">
						<span class="text-xs font-medium text-primary">{pub.date}</span>
						<h3 class="mt-1 text-sm font-bold text-dark group-hover:text-primary transition">
							{pub.title}
						</h3>
					</div>
				</a>
			{/each}
		</div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4 text-center">
		<h2 class="font-heading text-2xl font-bold text-dark">Recurring Events</h2>
		<div class="mt-8 grid grid-cols-1 gap-6 md:grid-cols-3">
			{#each recurringEvents as event (event.title)}
				<div class="rounded-xl bg-white p-6">
					<span class="text-xs font-medium uppercase tracking-wide text-primary">{event.frequency}</span>
					<h3 class="mt-2 font-heading text-lg font-bold text-dark">{event.title}</h3>
					<p class="mt-2 text-sm text-body">{event.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
