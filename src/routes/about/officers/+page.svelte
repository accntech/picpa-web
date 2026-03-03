<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';

	const boardArchives = [
		{ year: 'FY 2025-2026', open: true },
		{ year: 'FY 2024-2025', open: false },
		{ year: 'FY 2023-2024', open: false },
		{ year: 'FY 2022-2023', open: false },
		{ year: 'FY 2021-2022', open: false },
		{ year: 'FY 2020-2021', open: false },
		{ year: 'FY 2019-2020', open: false },
		{ year: 'FY 2018-2019', open: false },
		{ year: 'FY 2017-2018', open: false }
	];

	const sections = [
		{
			title: 'Chapter Presidents',
			desc: 'Local chapter leaders across 84 chapters nationwide'
		},
		{
			title: 'National Committees',
			desc: 'Specialized committees driving PICPA\'s initiatives and programs'
		},
		{
			title: 'Regional Representatives',
			desc: 'Representatives from 9 regions ensuring nationwide representation'
		},
		{
			title: 'National Secretariat',
			desc: 'The administrative team managing PICPA\'s day-to-day operations'
		}
	];
</script>

<PageHero
	title="Officers & Administration"
	breadcrumbs={[
		{ label: 'Home', href: '/' },
		{ label: 'About', href: '/about' },
		{ label: 'Officers' }
	]}
/>

<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-4 text-center">
		<h2 class="font-heading text-3xl font-bold text-dark">National Board of Directors</h2>
		<p class="mt-2 font-medium text-primary">FY 2025-2026</p>
		<div class="mt-8 overflow-hidden rounded-2xl shadow-lg">
			<img
				src="/images/officers/nbod-2025-2026.webp"
				alt="National Board of Directors FY 2025-2026"
				class="w-full"
			/>
		</div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-4xl px-4">
		<h2 class="text-center font-heading text-2xl font-bold text-dark">Board Archives</h2>
		<div class="mt-8 space-y-3">
			{#each boardArchives as archive (archive.year)}
				<details class="group bg-white rounded-xl overflow-hidden shadow-sm" open={archive.open}>
					<summary class="flex cursor-pointer items-center justify-between px-6 py-4 font-heading font-medium text-dark transition hover:text-primary">
						{archive.year}
						<svg
							class="h-5 w-5 shrink-0 transition-transform group-open:rotate-180"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="2"
							stroke="currentColor"
						>
							<path stroke-linecap="round" stroke-linejoin="round" d="M19.5 8.25l-7.5 7.5-7.5-7.5" />
						</svg>
					</summary>
					<div class="px-6 pb-4 text-body">
						Board of Directors for {archive.year}. View the complete list on the PICPA MELS portal.
					</div>
				</details>
			{/each}
		</div>
	</div>
</section>

<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-4">
		<div class="grid grid-cols-1 gap-6 md:grid-cols-2">
			{#each sections as section (section.title)}
				<div class="rounded-xl bg-light p-8">
					<h3 class="font-heading text-xl font-bold text-dark">{section.title}</h3>
					<p class="mt-2 text-body">{section.desc}</p>
					<p class="mt-4 text-sm font-medium text-primary">View on MELS Portal &rarr;</p>
				</div>
			{/each}
		</div>
	</div>
</section>
