<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';

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
			title: 'North America',
			locations: ['USA (East Coast)', 'USA (West Coast)', 'USA (Central)', 'Canada']
		},
		{
			title: 'Middle East',
			locations: ['UAE', 'Saudi Arabia', 'Qatar', 'Bahrain', 'Kuwait', 'Oman']
		},
		{
			title: 'Asia-Pacific',
			locations: ['Singapore', 'Hong Kong', 'Japan', 'Australia', 'Guam', 'Saipan', 'Palau']
		}
	];
</script>

<PageHero
	title="Local & International Chapters"
	breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'Chapters' }]}
/>

<section class="bg-white py-16">
	<div class="mx-auto max-w-4xl px-4">
		<div class="grid grid-cols-1 gap-8 text-center md:grid-cols-2">
			<div class="rounded-2xl bg-light p-10">
				<p class="font-heading text-5xl font-bold text-primary">84</p>
				<p class="mt-2 text-body">Local Chapters</p>
				<p class="text-sm text-body/70">across 9 regions</p>
			</div>
			<div class="rounded-2xl bg-light p-10">
				<p class="font-heading text-5xl font-bold text-gold">17</p>
				<p class="mt-2 text-body">International Chapters</p>
				<p class="text-sm text-body/70">worldwide</p>
			</div>
		</div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4">
		<div class="text-center">
			<h2 class="font-heading text-3xl font-bold text-dark">Regional Chapters</h2>
			<p class="mt-4 text-body">
				PICPA chapters organized across 9 regions in the Philippines
			</p>
		</div>

		<div class="mt-12 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each regions as region (region.name)}
				<div
					class="rounded-xl border border-transparent bg-white p-6 transition hover:border-primary/20 hover:shadow-md"
				>
					<h3 class="font-heading text-lg font-bold text-dark">{region.name}</h3>
					<p class="mt-1 text-sm text-body">{region.desc}</p>
					<div class="mt-4 flex items-center gap-2">
						<span class="h-2 w-2 rounded-full bg-primary"></span>
						<span class="text-sm font-medium text-primary">{region.count} chapters</span>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-4">
		<div class="text-center">
			<h2 class="font-heading text-3xl font-bold text-dark">International Chapters</h2>
			<p class="mt-4 text-body">
				PICPA's global presence connecting Filipino CPAs worldwide
			</p>
		</div>

		<div class="mt-12">
			{#each internationalGroups as group (group.title)}
				<div class="mb-10">
					<h3 class="mb-4 font-heading text-xl font-bold text-dark">{group.title}</h3>
					<div class="grid grid-cols-2 gap-4 md:grid-cols-4">
						{#each group.locations as location (location)}
							<div
								class="rounded-lg bg-light px-4 py-3 text-center text-sm font-medium text-dark transition hover:bg-primary/10"
							>
								{location}
							</div>
						{/each}
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
