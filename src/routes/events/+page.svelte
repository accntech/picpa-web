<script lang="ts">
	import PageHero from '$lib/components/PageHero.svelte';

	const featuredEvents = [
		{
			date: 'March 15-17, 2026',
			dayRange: '15-17',
			monthYear: 'March 2026',
			title: '81st Annual National Convention',
			location: 'Manila, Philippines',
			category: 'Convention',
			desc: 'The flagship event of PICPA bringing together CPAs from across the nation for three days of learning, networking, and professional development.'
		},
		{
			date: 'April 2026',
			dayRange: 'Apr',
			monthYear: '2026',
			title: 'National Tax Symposium',
			location: 'Virtual',
			category: 'Symposium',
			desc: 'A comprehensive symposium covering the latest tax regulations, compliance requirements, and best practices for Filipino CPAs.'
		},
		{
			date: 'May 2026',
			dayRange: 'May',
			monthYear: '2026',
			title: 'CPA Week Celebration',
			location: 'Nationwide',
			category: 'Celebration',
			desc: 'A week-long celebration recognizing the contributions of CPAs to the Philippine economy and society.'
		},
		{
			date: 'June 2026',
			dayRange: 'Jun',
			monthYear: '2026',
			title: 'Regional Leadership Summit',
			location: 'Cebu City',
			category: 'Summit',
			desc: 'Bringing together chapter leaders and regional officers to discuss strategic initiatives and share best practices.'
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

<PageHero title="Upcoming Events" breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'Events' }]} />

<section class="bg-primary/5 py-8">
	<div class="mx-auto flex max-w-7xl items-center gap-4 px-4">
		<svg class="h-6 w-6 shrink-0 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
			<circle cx="12" cy="12" r="10" />
			<line x1="12" y1="16" x2="12" y2="12" />
			<line x1="12" y1="8" x2="12.01" y2="8" />
		</svg>
		<p class="text-body">
			Events are managed through the PICPA Events System. Visit the external portal for complete event listings and registration.
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
		<h2 class="font-heading text-2xl font-bold text-dark">Featured Events</h2>
		<div class="mt-8 space-y-6">
			{#each featuredEvents as event (event.title)}
				<div class="flex flex-col gap-6 rounded-xl bg-light p-6 lg:flex-row">
					<div class="shrink-0 lg:w-40">
						<div class="rounded-xl bg-primary p-4 text-center text-white">
							<div class="text-2xl font-bold">{event.dayRange}</div>
							<div class="text-sm">{event.monthYear}</div>
						</div>
					</div>
					<div>
						<span class="inline-block rounded-full bg-primary/10 px-3 py-1 text-xs font-medium text-primary">
							{event.category}
						</span>
						<h3 class="mt-2 font-heading text-xl font-bold text-dark">{event.title}</h3>
						<p class="mt-1 flex items-center gap-1 text-sm text-body">
							<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
								<path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z" />
								<circle cx="12" cy="10" r="3" />
							</svg>
							{event.location}
						</p>
						<p class="mt-2 text-body">{event.desc}</p>
					</div>
				</div>
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
