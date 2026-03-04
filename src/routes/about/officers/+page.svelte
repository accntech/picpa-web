<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';

	interface Officer {
		name: string;
		position: string;
		region?: string;
		photo: string;
	}

	const president: Officer = {
		name: 'Gerard B. Sanvictores',
		position: 'National President',
		photo: '/images/officers/sanvictores.webp'
	};

	const executives: Officer[] = [
		{
			name: 'Dionisio M. Villeta',
			position: 'Executive Vice President',
			region: 'Western Visayas',
			photo: '/images/officers/villeta.webp'
		},
		{
			name: 'Henry M. Tan',
			position: 'VP for Operations',
			region: 'Metro Manila',
			photo: '/images/officers/tan-henry.webp'
		},
		{
			name: 'Consuelo O. Cadelina',
			position: 'Treasurer',
			region: 'Metro Manila',
			photo: '/images/officers/cadelina.webp'
		},
		{
			name: 'Mailene S. Bisnar',
			position: 'Secretary',
			region: 'Metro Manila',
			photo: '/images/officers/bisnar.webp'
		}
	];

	const vicePresidents: Officer[] = [
		{
			name: 'Ma. Elma I. Ame',
			position: 'VP for Public Practice',
			region: 'Southern Tagalog',
			photo: '/images/officers/ame.webp'
		},
		{
			name: 'Teresita A. Del Rosario',
			position: 'VP for Commerce & Industry',
			region: 'Metro Manila',
			photo: '/images/officers/del-rosario.webp'
		},
		{
			name: 'Angelita C. Ty',
			position: 'OIC-VP for Education',
			region: 'Southern Mindanao',
			photo: '/images/officers/ty.webp'
		},
		{
			name: 'Marylou C. Tan',
			position: 'VP for Government',
			region: 'Eastern Visayas',
			photo: '/images/officers/tan-marylou.webp'
		}
	];

	const regionalDirectors: Officer[] = [
		{ name: 'Jose M. Ireneo', position: 'Regional Director', region: 'Metro Manila', photo: '/images/officers/ireneo.webp' },
		{ name: 'Editha B. Tan', position: 'Regional Director', region: 'Northern Luzon', photo: '/images/officers/tan-editha.webp' },
		{ name: 'Constancia O. Molintas', position: 'Regional Director', region: 'Northern Luzon', photo: '/images/officers/molintas.webp' },
		{ name: 'Ronald S. Leabrres', position: 'Regional Director', region: 'Central Luzon', photo: '/images/officers/leabrres.webp' },
		{ name: 'Ferdinand J. San Diego', position: 'Regional Director', region: 'Central Luzon', photo: '/images/officers/san-diego.webp' },
		{ name: 'Sherryl B. Bool', position: 'Regional Director', region: 'Southern Tagalog', photo: '/images/officers/bool.webp' },
		{ name: 'Antonio G. Camalla', position: 'Regional Director', region: 'Bicol', photo: '/images/officers/camalla.webp' },
		{ name: 'Imelda M. Flores', position: 'Regional Director', region: 'Bicol', photo: '/images/officers/flores.webp' },
		{
			name: 'Atty. Pauline Grace T. Buñol',
			position: 'Regional Director',
			region: 'Western Visayas',
			photo: '/images/officers/bunol.webp'
		},
		{
			name: 'Atty. Bethuel G. Tanupan',
			position: 'Regional Director',
			region: 'Eastern Visayas',
			photo: '/images/officers/tanupan.webp'
		},
		{
			name: 'Jeserio G. Lonon, Jr.',
			position: 'Regional Director',
			region: 'Northern Mindanao',
			photo: '/images/officers/lonon.webp'
		},
		{
			name: 'Rowena B. Pag-ong Tabada',
			position: 'Regional Director',
			region: 'Northern Mindanao',
			photo: '/images/officers/tabada.webp'
		},
		{
			name: 'Jonas P. Mascariñas',
			position: 'Regional Director',
			region: 'Southern Mindanao',
			photo: '/images/officers/mascarinas.webp'
		}
	];

	const sectoralDirectors: Officer[] = [
		{ name: 'Editha A. Peralta', position: 'Sectoral Director', region: 'Education', photo: '/images/officers/peralta.webp' },
		{ name: 'Atty. Christina C. Barroga', position: 'Sectoral Director', region: 'Government', photo: '/images/officers/barroga.webp' },
		{
			name: 'Jessica Jinky P. Panes',
			position: 'Sectoral Director',
			region: 'Public Practice',
			photo: '/images/officers/panes.webp'
		}
	];

	const otherOfficers: Officer[] = [
		{ name: 'Atty. Roland C. Pondoc', position: 'Ex-Officio', photo: '/images/officers/pondoc.webp' },
		{ name: 'Geraldine H. Apostol', position: 'Executive Director', photo: '/images/officers/apostol.webp' }
	];

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

	let openIndex = $state(-1);

	const regionColorsLight: Record<string, string> = {
		'Metro Manila': 'bg-blue-50 text-blue-700',
		'Northern Luzon': 'bg-emerald-50 text-emerald-700',
		'Central Luzon': 'bg-amber-50 text-amber-700',
		'Southern Tagalog': 'bg-violet-50 text-violet-700',
		'Bicol': 'bg-rose-50 text-rose-700',
		'Western Visayas': 'bg-cyan-50 text-cyan-700',
		'Eastern Visayas': 'bg-teal-50 text-teal-700',
		'Northern Mindanao': 'bg-orange-50 text-orange-700',
		'Southern Mindanao': 'bg-indigo-50 text-indigo-700'
	};

	const sectorColors: Record<string, string> = {
		'Education': 'bg-primary/20 text-primary',
		'Government': 'bg-blue-500/15 text-blue-400',
		'Public Practice': 'bg-amber-500/15 text-amber-400'
	};
</script>

<svelte:head>
	<style>
		.officer-photo {
			position: relative;
			overflow: hidden;
		}
		.officer-photo img {
			transition: transform 0.6s cubic-bezier(0.22, 1, 0.36, 1);
		}
		.officer-photo:hover img,
		.officer-card:hover .officer-photo img {
			transform: scale(1.08);
		}
		.officer-photo::after {
			content: '';
			position: absolute;
			inset: 0;
			background: linear-gradient(to top, rgba(10, 15, 26, 0.5) 0%, transparent 50%);
			opacity: 0;
			transition: opacity 0.4s ease;
		}
		.officer-card:hover .officer-photo::after {
			opacity: 1;
		}
		.president-frame {
			position: relative;
		}
		.president-frame::before {
			content: '';
			position: absolute;
			inset: -4px;
			border-radius: 1.5rem;
			background: linear-gradient(135deg, #18b355 0%, #0d6e35 40%, #d4a843 100%);
			z-index: -1;
		}
		.exec-portrait {
			position: relative;
		}
		.exec-portrait::before {
			content: '';
			position: absolute;
			inset: -3px;
			border-radius: 1rem;
			background: linear-gradient(160deg, #18b355, transparent 60%);
			z-index: -1;
			opacity: 0;
			transition: opacity 0.4s ease;
		}
		.officer-card:hover .exec-portrait::before {
			opacity: 1;
		}
	</style>
</svelte:head>

<PageHero
	title="National Board of Directors"
	breadcrumbs={[
		{ label: 'Home', href: '/' },
		{ label: 'About', href: '/about' },
		{ label: 'Officers' }
	]}
/>

<!-- PRESIDENT -->
<section class="relative overflow-hidden bg-navy py-28 lg:py-36">
	<div class="gradient-mesh-bg absolute inset-0"></div>

	<svg class="absolute -top-8 -right-12 h-72 w-72 text-white/3" style="animation: float 6s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>
	<svg class="absolute -bottom-6 -left-8 h-48 w-48 text-white/3" style="animation: float-reverse 7s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="flex flex-col items-center gap-10 lg:flex-row lg:gap-20">
				<div class="shrink-0">
					<div class="president-frame">
						<div class="officer-photo h-52 w-52 rounded-3xl lg:h-64 lg:w-64" style="animation: pulse-glow 3s ease-in-out infinite;">
							<img src={president.photo} alt={president.name} class="h-full w-full rounded-3xl object-cover" />
						</div>
					</div>
				</div>
				<div class="text-center lg:text-left">
					<span class="inline-block rounded-full bg-primary/15 px-4 py-1.5 text-xs font-semibold uppercase tracking-widest text-primary">
						FY 2025-2026
					</span>
					<h2 class="mt-5 font-heading text-[clamp(1.75rem,4vw,3rem)] font-bold leading-tight text-white">
						{president.name}
					</h2>
					<p class="mt-3 text-xl font-medium text-primary">
						{president.position}
					</p>
					<div class="mt-6 flex items-center justify-center gap-1.5 text-slate lg:justify-start">
						<svg class="h-4 w-4 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
							<polyline points="13 17 18 12 13 7" />
							<polyline points="6 17 11 12 6 7" />
						</svg>
						<span class="text-sm">Leading the Philippine Institute of Certified Public Accountants</span>
					</div>
				</div>
			</div>
		</ScrollReveal>
	</div>
</section>

<!-- EXECUTIVE OFFICERS -->
<section class="bg-white py-28">
	<div class="mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="max-w-2xl">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Leadership</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold leading-tight text-dark">
					Executive Officers
				</h2>
			</div>
		</ScrollReveal>

		<div class="mt-16 grid grid-cols-2 gap-8 lg:grid-cols-4 lg:gap-10">
			{#each executives as officer, i (officer.name)}
				<ScrollReveal stagger={i}>
					<div class="officer-card group">
						<div class="exec-portrait">
							<div class="officer-photo aspect-[3/4] w-full rounded-2xl bg-light">
								<img
									src={officer.photo}
									alt={officer.name}
									class="h-full w-full rounded-2xl object-cover object-top"
								/>
							</div>
						</div>
						<div class="mt-5">
							<h3 class="font-heading text-lg font-bold leading-snug text-dark">{officer.name}</h3>
							<p class="mt-1 text-sm font-semibold text-primary">{officer.position}</p>
							{#if officer.region}
								<p class="mt-1 text-xs text-body">Regional Director, {officer.region}</p>
							{/if}
						</div>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<!-- NATIONAL VICE PRESIDENTS -->
<section class="bg-light py-28">
	<div class="mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="max-w-2xl">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Sector Heads</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold leading-tight text-dark">
					National Vice Presidents
				</h2>
			</div>
		</ScrollReveal>

		<div class="mt-16 grid grid-cols-2 gap-8 lg:grid-cols-4 lg:gap-10">
			{#each vicePresidents as officer, i (officer.name)}
				<ScrollReveal stagger={i}>
					<div class="officer-card group">
						<div class="exec-portrait">
							<div class="officer-photo aspect-[3/4] w-full rounded-2xl bg-white">
								<img
									src={officer.photo}
									alt={officer.name}
									class="h-full w-full rounded-2xl object-cover object-top"
								/>
							</div>
						</div>
						<div class="mt-5">
							<h3 class="font-heading text-lg font-bold leading-snug text-dark">{officer.name}</h3>
							<p class="mt-1 text-sm font-semibold text-primary">{officer.position}</p>
							{#if officer.region}
								<p class="mt-1 text-xs text-body">Regional Director, {officer.region}</p>
							{/if}
						</div>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<!-- REGIONAL DIRECTORS -->
<section class="bg-white py-28">
	<div class="mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="max-w-2xl">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Nationwide Reach</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold leading-tight text-dark">
					Regional Directors
				</h2>
			</div>
		</ScrollReveal>

		<div class="mt-16 grid grid-cols-2 gap-x-6 gap-y-10 sm:grid-cols-3 lg:grid-cols-4 xl:gap-x-8">
			{#each regionalDirectors as officer, i (officer.name)}
				<ScrollReveal stagger={i}>
					<div class="officer-card group text-center">
						<div class="mx-auto w-full max-w-[180px]">
							<div class="officer-photo aspect-square w-full rounded-2xl bg-light">
								<img
									src={officer.photo}
									alt={officer.name}
									class="h-full w-full rounded-2xl object-cover"
								/>
							</div>
						</div>
						<h3 class="mt-4 font-heading text-sm font-bold leading-snug text-dark">{officer.name}</h3>
						{#if officer.region}
							<span class="mt-2 inline-block rounded-full px-2.5 py-0.5 text-[11px] font-semibold {regionColorsLight[officer.region] ?? 'bg-gray-50 text-gray-600'}">
								{officer.region}
							</span>
						{/if}
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<!-- SECTORAL DIRECTORS -->
<section class="relative overflow-hidden bg-navy py-28">
	<div class="gradient-mesh-bg absolute inset-0"></div>

	<svg class="absolute top-10 right-10 h-40 w-40 text-white/3" style="animation: float 6s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-5xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Sector Representation</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">
					Sectoral Directors
				</h2>
			</div>
		</ScrollReveal>

		<div class="mx-auto mt-16 grid max-w-4xl grid-cols-1 gap-10 sm:grid-cols-3">
			{#each sectoralDirectors as officer, i (officer.name)}
				<ScrollReveal stagger={i}>
					<div class="officer-card group text-center">
						<div class="mx-auto w-full max-w-[200px]">
							<div class="officer-photo aspect-square w-full rounded-2xl ring-1 ring-white/10">
								<img
									src={officer.photo}
									alt={officer.name}
									class="h-full w-full rounded-2xl object-cover"
								/>
							</div>
						</div>
						<h3 class="mt-5 font-heading text-base font-bold text-white">{officer.name}</h3>
						{#if officer.region}
							<span class="mt-2 inline-block rounded-full px-3 py-1 text-xs font-semibold {sectorColors[officer.region] ?? 'bg-white/10 text-slate'}">
								{officer.region}
							</span>
						{/if}
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<!-- OTHER OFFICERS -->
<section class="bg-white py-28">
	<div class="mx-auto max-w-4xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Administration</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-dark">
					Other Officers
				</h2>
			</div>
		</ScrollReveal>

		<div class="mx-auto mt-16 grid max-w-md grid-cols-2 gap-10">
			{#each otherOfficers as officer, i (officer.name)}
				<ScrollReveal stagger={i}>
					<div class="officer-card group text-center">
						<div class="mx-auto w-full max-w-[180px]">
							<div class="officer-photo aspect-square w-full rounded-2xl bg-light">
								<img
									src={officer.photo}
									alt={officer.name}
									class="h-full w-full rounded-2xl object-cover"
								/>
							</div>
						</div>
						<h3 class="mt-4 font-heading text-base font-bold text-dark">{officer.name}</h3>
						<p class="mt-1 text-sm font-medium text-body">{officer.position}</p>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<!-- BOARD ARCHIVES -->
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
