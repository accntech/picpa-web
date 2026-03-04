<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';

	const programs = [
		{
			title: 'Research & Development',
			desc: 'Funding and supporting research initiatives that advance accounting knowledge and practice in the Philippines.'
		},
		{
			title: 'Professional Development',
			desc: 'Programs designed to enhance the skills and competencies of Filipino CPAs across all sectors.'
		},
		{
			title: 'Scholarships',
			desc: 'Providing financial assistance to deserving accounting students to pursue their education and career goals.'
		},
		{
			title: 'Ayuda sa Escuela',
			desc: 'A community outreach program providing support to schools and educational institutions across the country.'
		}
	];

	const founders = [
		{ name: 'Jaime C. Laya', subtitle: 'Former BSP Governor' },
		{ name: 'Washington A. SyCip', subtitle: 'Founder, SGV & Co.' },
		{ name: 'Roberto Ongpin', subtitle: 'Business Leader' }
	];
</script>

<PageHero
	title="PICPA Foundation"
	breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'Foundation' }]}
/>

<section class="relative overflow-hidden bg-white py-24">
	<svg class="absolute -top-10 -right-10 h-80 w-80 text-primary/3" style="animation: float 8s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<div class="grid grid-cols-1 items-center gap-16 lg:grid-cols-2">
			<ScrollReveal direction="left">
				<img
					src="/images/foundation/logo.jpg"
					alt="PICPA Foundation Logo"
					class="rounded-2xl shadow-xl"
				/>
			</ScrollReveal>

			<ScrollReveal direction="right" delay={100}>
				<span class="inline-block rounded-full bg-gold/10 px-4 py-1.5 text-sm font-medium text-gold">
					Established December 29, 1981
				</span>
				<h2 class="mt-5 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold leading-tight text-dark">
					PICPA Foundation Inc.
				</h2>
				<p class="mt-5 text-lg leading-relaxed text-body">
					The PICPA Foundation, Inc. was established to support the advancement of the accountancy
					profession in the Philippines through research, professional development, scholarships, and
					community service programs.
				</p>
				<p class="mt-4 text-body">
					The Foundation is accredited by the Philippine Council for NGO Certification (PCNC) and
					holds Donee Institution status, enabling it to receive tax-deductible donations.
				</p>
				<div class="mt-6 flex items-center gap-2 text-sm font-medium text-primary">
					<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
						<polyline points="13 17 18 12 13 7" />
						<polyline points="6 17 11 12 6 7" />
					</svg>
					PCNC Accredited &bull; Donee Institution
				</div>
			</ScrollReveal>
		</div>
	</div>
</section>

<section class="relative overflow-hidden bg-navy py-24">
	<div class="gradient-mesh-bg absolute inset-0"></div>

	<svg class="absolute -bottom-8 -left-8 h-64 w-64 text-white/3" style="animation: float-reverse 7s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<h2 class="font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">
				Our Programs
			</h2>
			<div class="mt-2 h-1 w-12 rounded-full bg-primary"></div>
		</ScrollReveal>

		<div class="mt-14 grid grid-cols-1 gap-8 md:grid-cols-2">
			{#each programs as program, i (program.title)}
				<ScrollReveal stagger={i}>
					<div class="glass rounded-2xl p-8 transition-transform duration-300 hover:-translate-y-1" style="transition-timing-function: cubic-bezier(0.22, 1, 0.36, 1);">
						{#if i === 0}
							<svg class="h-10 w-10 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
								<path stroke-linecap="round" stroke-linejoin="round" d="M9.75 3.104v5.714a2.25 2.25 0 01-.659 1.591L5 14.5M9.75 3.104c-.251.023-.501.05-.75.082m.75-.082a24.301 24.301 0 014.5 0m0 0v5.714c0 .597.237 1.17.659 1.591L19.8 14.5M14.25 3.104c.251.023.501.05.75.082M19.8 14.5l-2.098 4.196a2.25 2.25 0 01-2.013 1.242h-7.378a2.25 2.25 0 01-2.013-1.242L4.2 14.5m15.6 0h-15.6" />
							</svg>
						{:else if i === 1}
							<svg class="h-10 w-10 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
								<path stroke-linecap="round" stroke-linejoin="round" d="M2.25 18L9 11.25l4.306 4.307a11.95 11.95 0 015.814-5.519l2.74-1.22m0 0l-5.94-2.28m5.94 2.28l-2.28 5.941" />
							</svg>
						{:else if i === 2}
							<svg class="h-10 w-10 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
								<path stroke-linecap="round" stroke-linejoin="round" d="M4.26 10.147a60.436 60.436 0 00-.491 6.347A48.627 48.627 0 0112 20.904a48.627 48.627 0 018.232-4.41 60.46 60.46 0 00-.491-6.347m-15.482 0a50.57 50.57 0 00-2.658-.813A59.905 59.905 0 0112 3.493a59.902 59.902 0 0110.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.697 50.697 0 0112 13.489a50.702 50.702 0 017.74-3.342M6.75 15a.75.75 0 100-1.5.75.75 0 000 1.5zm0 0v-3.675A55.378 55.378 0 0112 8.443m-7.007 11.55A5.981 5.981 0 006.75 15.75v-1.5" />
							</svg>
						{:else}
							<svg class="h-10 w-10 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
								<path stroke-linecap="round" stroke-linejoin="round" d="M12 21v-8.25M15.75 21v-8.25M8.25 21v-8.25M3 9l9-6 9 6m-1.5 12V10.332A48.36 48.36 0 0012 9.75c-2.551 0-5.056.2-7.5.582V21M3 21h18M12 6.75h.008v.008H12V6.75z" />
							</svg>
						{/if}
						<h3 class="mt-5 font-heading text-xl font-bold text-white">{program.title}</h3>
						<p class="mt-3 leading-relaxed text-slate">{program.desc}</p>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="relative overflow-hidden bg-white py-24">
	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<div class="grid grid-cols-1 items-center gap-16 lg:grid-cols-2">
			<ScrollReveal direction="left">
				<span class="inline-flex items-center gap-2 rounded-full bg-primary/10 px-4 py-1.5 text-sm font-medium text-primary">
					<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
						<path stroke-linecap="round" stroke-linejoin="round" d="M16.5 18.75h-9m9 0a3 3 0 013 3h-15a3 3 0 013-3m9 0v-4.5A3.375 3.375 0 0012.75 11h-1.5A3.375 3.375 0 007.875 14.25v4.5m8.625 0h-8.625" />
					</svg>
					Premier Recognition Program
				</span>
				<h2 class="mt-5 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold leading-tight text-dark">
					Parangal San Mateo Awards
				</h2>
				<p class="mt-5 text-lg leading-relaxed text-body">
					The Parangal San Mateo Awards is the PICPA Foundation's premier recognition program,
					honoring outstanding CPAs who have made significant contributions to the accountancy
					profession and to society.
				</p>
				<p class="mt-4 text-body">
					Named after Saint Matthew, the patron saint of accountants, these awards celebrate
					excellence, integrity, and service.
				</p>
				<ul class="mt-6 space-y-3">
					<li class="flex items-start gap-3 text-body">
						<svg class="mt-0.5 h-5 w-5 shrink-0 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
							<polyline points="13 17 18 12 13 7" />
							<polyline points="6 17 11 12 6 7" />
						</svg>
						Outstanding contributions to the profession
					</li>
					<li class="flex items-start gap-3 text-body">
						<svg class="mt-0.5 h-5 w-5 shrink-0 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
							<polyline points="13 17 18 12 13 7" />
							<polyline points="6 17 11 12 6 7" />
						</svg>
						Excellence, integrity, and service
					</li>
					<li class="flex items-start gap-3 text-body">
						<svg class="mt-0.5 h-5 w-5 shrink-0 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
							<polyline points="13 17 18 12 13 7" />
							<polyline points="6 17 11 12 6 7" />
						</svg>
						Named after the patron saint of accountants
					</li>
				</ul>
			</ScrollReveal>

			<ScrollReveal direction="right" delay={100}>
				<img
					src="/images/foundation/parangal.png"
					alt="Parangal San Mateo Awards"
					class="mx-auto max-h-125 rounded-2xl object-contain shadow-xl"
				/>
			</ScrollReveal>
		</div>
	</div>
</section>

<section class="relative overflow-hidden bg-navy py-24">
	<div class="gradient-mesh-bg absolute inset-0"></div>

	<svg class="absolute top-8 right-12 h-40 w-40 text-white/3" style="animation: float 6s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<h2 class="font-heading text-[clamp(1.5rem,2.5vw,2rem)] font-bold text-white">
					Recognition & Accreditation
				</h2>
				<div class="mx-auto mt-3 h-1 w-12 rounded-full bg-primary"></div>
			</div>
		</ScrollReveal>

		<div class="mx-auto mt-14 grid max-w-4xl grid-cols-1 gap-8 md:grid-cols-2">
			<ScrollReveal stagger={0}>
				<div class="glass rounded-2xl p-8 text-center">
					<svg class="mx-auto h-10 w-10 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
						<path stroke-linecap="round" stroke-linejoin="round" d="M9 12.75L11.25 15 15 9.75m-3-7.036A11.959 11.959 0 013.598 6 11.99 11.99 0 003 9.749c0 5.592 3.824 10.29 9 11.623 5.176-1.332 9-6.03 9-11.622 0-1.31-.21-2.571-.598-3.751h-.152c-3.196 0-6.1-1.248-8.25-3.285z" />
					</svg>
					<h3 class="mt-4 font-heading text-xl font-bold text-white">PCNC Accredited</h3>
					<p class="mt-3 leading-relaxed text-slate">
						Accredited by the Philippine Council for NGO Certification, recognizing our adherence to
						the highest standards of non-profit governance.
					</p>
				</div>
			</ScrollReveal>
			<ScrollReveal stagger={1}>
				<div class="glass rounded-2xl p-8 text-center">
					<svg class="mx-auto h-10 w-10 text-gold" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
						<path stroke-linecap="round" stroke-linejoin="round" d="M19.5 14.25v-2.625a3.375 3.375 0 00-3.375-3.375h-1.5A1.125 1.125 0 0113.5 7.125v-1.5a3.375 3.375 0 00-3.375-3.375H8.25m0 12.75h7.5m-7.5 3H12M10.5 2.25H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 00-9-9z" />
					</svg>
					<h3 class="mt-4 font-heading text-xl font-bold text-white">Donee Institution</h3>
					<p class="mt-3 leading-relaxed text-slate">
						Granted Donee Institution status by the Bureau of Internal Revenue, enabling
						tax-deductible donations.
					</p>
				</div>
			</ScrollReveal>
		</div>

		<ScrollReveal delay={200}>
			<div class="mt-12 text-center">
				<img
					src="/images/foundation/donee-certificate.png"
					alt="Donee Institution Certificate"
					class="mx-auto w-full max-w-sm rounded-xl shadow-lg ring-1 ring-white/10"
				/>
			</div>
		</ScrollReveal>
	</div>
</section>

<section class="bg-white py-24">
	<div class="mx-auto max-w-5xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<h2 class="font-heading text-[clamp(1.5rem,2.5vw,2rem)] font-bold text-dark">
					Notable Founders
				</h2>
				<p class="mx-auto mt-4 max-w-2xl text-lg text-body">
					The PICPA Foundation was established through the vision of prominent Filipino leaders:
				</p>
			</div>
		</ScrollReveal>

		<div class="mt-12 grid grid-cols-1 gap-8 md:grid-cols-3">
			{#each founders as founder, i (founder.name)}
				<ScrollReveal stagger={i}>
					<div class="group rounded-2xl bg-white p-8 text-center shadow-md ring-1 ring-black/5 transition-all duration-300 hover:-translate-y-1 hover:shadow-xl" style="transition-timing-function: cubic-bezier(0.22, 1, 0.36, 1);">
						<div class="mx-auto flex h-14 w-14 items-center justify-center rounded-xl bg-primary/10">
							<svg class="h-7 w-7 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
								<path stroke-linecap="round" stroke-linejoin="round" d="M15.75 6a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0zM4.501 20.118a7.5 7.5 0 0114.998 0A17.933 17.933 0 0112 21.75c-2.676 0-5.216-.584-7.499-1.632z" />
							</svg>
						</div>
						<p class="mt-5 font-heading text-lg font-bold text-dark">{founder.name}</p>
						<p class="mt-1 text-sm text-body">{founder.subtitle}</p>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="bg-light py-24">
	<div class="mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<h2 class="font-heading text-[clamp(1.5rem,2.5vw,2rem)] font-bold text-dark">
					Board of Trustees
				</h2>
				<p class="mt-2 text-body">FY 2024-2025</p>
			</div>
		</ScrollReveal>

		<ScrollReveal delay={100}>
			<img
				src="/images/foundation/board.png"
				alt="PICPA Foundation Board of Trustees"
				class="mt-12 w-full rounded-2xl shadow-lg"
			/>
		</ScrollReveal>

		<ScrollReveal delay={200}>
			<img
				src="/images/foundation/committee.png"
				alt="PICPA Foundation Committee Members"
				class="mt-8 w-full rounded-2xl shadow-lg"
			/>
		</ScrollReveal>

		<p class="mt-6 text-center text-sm text-body">
			PICPA Foundation Board of Trustees and Committee Members
		</p>
	</div>
</section>
