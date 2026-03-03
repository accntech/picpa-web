<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';

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

<section class="bg-white py-20">
	<div class="mx-auto grid max-w-7xl grid-cols-1 items-start gap-12 px-4 lg:grid-cols-3">
		<div class="lg:col-span-1">
			<img
				src="/images/president/gbs3.png"
				alt="Gerard B. Sanvictores"
				class="w-full rounded-2xl shadow-lg"
			/>
			<div class="mt-4 text-center">
				<p class="font-heading text-xl font-bold text-dark">Gerard B. Sanvictores</p>
				<p class="text-sm text-body">National President, FY 2025-2026</p>
			</div>
		</div>

		<div class="lg:col-span-2">
			<span class="inline-block rounded-full bg-gold/10 px-4 py-1.5 text-sm font-medium text-gold">
				FY 2025-2026 Theme
			</span>
			<h2 class="mt-4 font-heading text-4xl font-bold text-dark lg:text-5xl">
				ACTION with IMPACT
			</h2>
			<div class="mt-6 h-1 w-20 bg-primary"></div>
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
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="text-center font-heading text-2xl font-bold text-dark">ACTION</h2>
		<p class="mt-2 text-center text-body">The pillars of our proactive approach</p>

		<div class="mt-12 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each actionCards as card (card.letter + card.word)}
				<div class="rounded-xl bg-white p-6 shadow-sm">
					<p class="font-heading text-4xl font-bold text-primary">{card.letter}</p>
					<p class="mt-2 font-heading text-lg font-bold text-dark">{card.word}</p>
					<p class="mt-2 text-sm text-body">{card.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="text-center font-heading text-2xl font-bold text-dark">IMPACT</h2>
		<p class="mt-2 text-center text-body">The values that define our outcomes</p>

		<div class="mt-12 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each impactCards as card (card.letter + card.word)}
				<div class="rounded-xl bg-light p-6">
					<p class="font-heading text-4xl font-bold text-primary">{card.letter}</p>
					<p class="mt-2 font-heading text-lg font-bold text-dark">{card.word}</p>
					<p class="mt-2 text-sm text-body">{card.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
