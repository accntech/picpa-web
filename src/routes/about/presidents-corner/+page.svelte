<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';

	const actionCards = [
		{ letter: 'A', word: 'Adapt', desc: 'Embrace change and evolve with the dynamic demands of the profession' },
		{ letter: 'C', word: 'Commit', desc: 'Dedicate ourselves to the highest standards of professional excellence' },
		{ letter: 'T', word: 'Transform', desc: 'Drive meaningful transformation in accounting practices and education' },
		{ letter: 'I', word: 'Innovate', desc: 'Pioneer new approaches and leverage technology for progress' },
		{ letter: 'O', word: 'Optimize', desc: 'Maximize our resources and processes for greater efficiency' },
		{ letter: 'N', word: 'Nurture', desc: 'Foster growth, mentorship, and development among members' }
	];

	const impactCards = [
		{ letter: 'I', word: 'Integrity', desc: 'Upholding the highest ethical standards in everything we do' },
		{ letter: 'M', word: 'Merit', desc: 'Recognizing excellence and rewarding outstanding achievements' },
		{ letter: 'P', word: 'Professionalism', desc: 'Maintaining the highest standards of professional conduct' },
		{ letter: 'A', word: 'Accountability', desc: 'Being responsible and transparent in all our actions' },
		{ letter: 'C', word: 'Competence', desc: 'Continuously developing skills and expertise' },
		{ letter: 'T', word: 'Teamwork', desc: 'Collaborating effectively to achieve shared goals' }
	];
</script>

<PageHero
	title="President's Corner"
	breadcrumbs={[
		{ label: 'Home', href: '/' },
		{ label: 'About', href: '/about' },
		{ label: "President's Corner" }
	]}
/>

<section class="bg-white py-24">
	<div class="mx-auto max-w-7xl px-4 lg:px-8">
		<div class="grid grid-cols-1 items-start gap-12 lg:grid-cols-5">
			<ScrollReveal direction="left">
				<div class="relative lg:col-span-2">
					<div class="relative overflow-hidden rounded-2xl">
						<img
							src="/images/president/gbs3.png"
							alt="Gerard B. Sanvictores"
							class="w-full"
						/>
						<div class="pointer-events-none absolute inset-0 bg-linear-to-r from-transparent via-transparent to-white/60"></div>
						<div class="pointer-events-none absolute inset-0 bg-linear-to-t from-navy/40 via-transparent to-transparent"></div>
					</div>
					<div class="mt-5 text-center">
						<p class="font-heading text-xl font-bold text-dark">Gerard B. Sanvictores</p>
						<p class="mt-1 text-sm text-body">National President, FY 2025-2026</p>
					</div>
				</div>
			</ScrollReveal>

			<ScrollReveal direction="right" delay={100}>
				<div class="lg:col-span-3">
					<span class="inline-block rounded-full bg-gold/10 px-4 py-1.5 text-sm font-medium text-gold">
						FY 2025-2026 Theme
					</span>
					<h2 class="mt-5 font-heading text-[clamp(2rem,4vw,3rem)] font-bold leading-tight text-dark">
						ACTION with IMPACT
					</h2>
					<div class="mt-5 h-1 w-20 rounded-full bg-primary"></div>
					<p class="mt-6 leading-relaxed text-body">
						As we embark on this new fiscal year, I am honored to lead the Philippine Institute of
						Certified Public Accountants under the theme 'ACTION with IMPACT.' This theme encapsulates
						our commitment to proactive engagement and meaningful contributions to the accountancy
						profession and society at large.
					</p>
					<p class="mt-4 leading-relaxed text-body">
						Our vision for FY 2025-2026 is to strengthen PICPA's role as a globally relevant
						professional organization while ensuring that every initiative we undertake creates lasting
						positive change for our members and stakeholders.
					</p>
				</div>
			</ScrollReveal>
		</div>
	</div>
</section>

<section class="bg-light py-16">
	<div class="mx-auto max-w-3xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="flex items-start justify-center gap-4">
				<svg class="mt-1 h-10 w-8 shrink-0 text-primary/30" viewBox="0 0 87 85" fill="currentColor">
					<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
					<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
					<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
					<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
				</svg>
				<p class="text-center font-heading text-[clamp(1.1rem,2vw,1.4rem)] font-medium leading-relaxed text-dark/80 italic">
					Every initiative we undertake must create lasting positive change for our members, the profession, and the communities we serve.
				</p>
				<svg class="mt-1 h-10 w-8 shrink-0 text-primary/30" viewBox="0 0 87 85" fill="currentColor">
					<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
					<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
					<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
					<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
				</svg>
			</div>
			<p class="mt-4 text-center text-sm font-medium text-primary">
				Gerard B. Sanvictores, CPA
			</p>
		</ScrollReveal>
	</div>
</section>

<section class="relative bg-navy py-24">
	<div class="gradient-mesh-bg absolute inset-0"></div>

	<svg class="absolute top-8 right-12 h-36 w-36 text-white/3" style="animation: float 6s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Pillars</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">
					ACTION
				</h2>
				<p class="mt-2 text-slate">The pillars of our proactive approach</p>
			</div>
		</ScrollReveal>

		<div class="mt-14 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each actionCards as card, i (card.letter + card.word)}
				<ScrollReveal stagger={i}>
					<div class="glass rounded-2xl p-8 transition-all duration-300 hover:-translate-y-1 hover:border-primary/20">
						<p class="bg-linear-to-br from-primary to-primary-dark bg-clip-text font-heading text-5xl font-bold text-transparent">
							{card.letter}
						</p>
						<p class="mt-3 font-heading text-lg font-bold text-white">{card.word}</p>
						<p class="mt-2 leading-relaxed text-slate">{card.desc}</p>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="relative bg-navy-mid py-24">
	<div class="gradient-mesh-bg absolute inset-0 opacity-50"></div>

	<svg class="absolute bottom-8 left-12 h-32 w-32 text-white/3" style="animation: float-reverse 7s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Values</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">
					IMPACT
				</h2>
				<p class="mt-2 text-slate">The values that define our outcomes</p>
			</div>
		</ScrollReveal>

		<div class="mt-14 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each impactCards as card, i (card.letter + card.word)}
				<ScrollReveal stagger={i}>
					<div class="glass rounded-2xl p-8 transition-all duration-300 hover:-translate-y-1 hover:border-primary/20">
						<p class="bg-linear-to-br from-gold to-gold/60 bg-clip-text font-heading text-5xl font-bold text-transparent">
							{card.letter}
						</p>
						<p class="mt-3 font-heading text-lg font-bold text-white">{card.word}</p>
						<p class="mt-2 leading-relaxed text-slate">{card.desc}</p>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>
