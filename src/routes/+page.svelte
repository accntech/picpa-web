<script lang="ts">
	import StatsBar from '$lib/components/StatsBar.svelte';
	import AnnouncementCard from '$lib/components/AnnouncementCard.svelte';
	import ScrollReveal from '$lib/components/ScrollReveal.svelte';

	const actionWords = ['Adapt', 'Commit', 'Transform', 'Innovate', 'Optimize', 'Nurture'];
	const impactWords = ['Integrity', 'Merit', 'Professionalism', 'Accountability', 'Competence', 'Teamwork'];

	const announcements = [
		{
			image: '/images/announcements/coffee-table-book.webp',
			date: 'February 2025',
			title: 'PICPA Foundation Coffee Table Book Wins Silver at 60th Anvil Awards',
			excerpt: "The PICPA Foundation's commemorative coffee table book has been recognized with a Silver Award at the prestigious 60th Anvil Awards."
		},
		{
			image: '/images/announcements/admin-announcement.jpg',
			date: 'December 2025',
			title: 'PICPA National Elections 2025 Results',
			excerpt: 'The official results of the PICPA National Elections for FY 2025-2026 have been announced.'
		},
		{
			image: '/images/announcements/announcement-photo.webp',
			date: 'December 2025',
			title: 'PICPA Recognized at Malacanang Palace',
			excerpt: "PICPA officers were received at Malacanang Palace in recognition of the organization's contributions to the profession."
		},
		{
			image: '/images/announcements/moe-document.jpg',
			date: 'January 2026',
			title: '6th National Summit on Government Procurement',
			excerpt: 'PICPA hosts the 6th National Summit focusing on government procurement best practices and transparency.'
		},
		{
			image: '/images/announcements/accounting-times-sept.webp',
			date: 'September 2025',
			title: 'Accounting Times September 2025 Edition',
			excerpt: 'The latest edition of the Accounting Times features articles on emerging trends in Philippine accountancy.'
		},
		{
			image: '/images/announcements/accounting-times.webp',
			date: 'July 2023',
			title: 'Accounting Times Publication Archive',
			excerpt: 'Browse the collection of past Accounting Times editions covering key developments in the profession.'
		}
	];

	const programs = ['Research & Development', 'Professional Development', 'Scholarships', 'Ayuda sa Escuela'];
</script>

<div class="pt-0">
	<!-- Hero -->
	<section
		class="relative flex min-h-screen items-center justify-center bg-primary-deep"
		style="background: radial-gradient(ellipse at center, rgba(24, 179, 85, 0.08) 0%, #0a1f13 70%)"
	>
		<img
			src="/images/logos/emblem.png"
			alt=""
			class="pointer-events-none absolute h-[500px] w-[500px] opacity-5"
		/>
		<div class="relative z-10 px-4 text-center">
			<p class="text-sm font-medium uppercase tracking-widest text-gold">EST. 1929</p>
			<h1 class="mx-auto mt-4 max-w-4xl font-heading text-5xl font-bold leading-tight text-white lg:text-7xl">
				Philippine Institute of Certified Public Accountants
			</h1>
			<p class="mx-auto mt-6 max-w-2xl text-lg text-white/80 lg:text-xl">
				The National Organization of Certified Public Accountants
			</p>
			<p class="mt-4 font-medium text-gold">
				Awarded five times as PRC's most outstanding AIPO
			</p>
			<div class="mt-10 flex justify-center gap-4">
				<a
					href="/members"
					class="rounded-lg bg-primary px-8 py-3.5 font-medium text-white transition hover:bg-primary-dark"
				>
					Become a Member
				</a>
				<a
					href="/about"
					class="rounded-lg border-2 border-white px-8 py-3.5 font-medium text-white transition hover:bg-white hover:text-dark"
				>
					Learn More
				</a>
			</div>
		</div>
	</section>

	<!-- Stats -->
	<ScrollReveal><StatsBar /></ScrollReveal>

	<!-- President's Section -->
	<section class="bg-white py-20">
		<ScrollReveal>
			<div class="mx-auto grid max-w-7xl grid-cols-1 items-center gap-12 px-4 lg:grid-cols-2">
				<div class="relative">
					<div class="absolute -right-4 -bottom-4 -z-10 h-full w-full rounded-2xl bg-primary/20"></div>
					<img
						src="/images/president/gbs1.png"
						alt="Gerard B. Sanvictores"
						class="relative rounded-2xl border-4 border-primary/20 object-cover"
					/>
				</div>
				<div>
					<span class="inline-block rounded-full bg-primary/10 px-4 py-1.5 text-sm font-medium text-primary">
						FY 2025-2026
					</span>
					<h2 class="mt-4 font-heading text-3xl font-bold text-dark">Gerard B. Sanvictores</h2>
					<p class="mt-1 text-body">National President</p>
					<p class="mt-6 font-heading text-2xl font-bold text-primary-dark">ACTION with IMPACT</p>
					<div class="mt-8 grid grid-cols-2 gap-6">
						<div class="space-y-2">
							{#each actionWords as word (word)}
								<div class="flex items-center gap-2">
									<span class="h-2 w-2 rounded-full bg-primary"></span>
									<span class="text-body">{word}</span>
								</div>
							{/each}
						</div>
						<div class="space-y-2">
							{#each impactWords as word (word)}
								<div class="flex items-center gap-2">
									<span class="h-2 w-2 rounded-full bg-primary"></span>
									<span class="text-body">{word}</span>
								</div>
							{/each}
						</div>
					</div>
				</div>
			</div>
		</ScrollReveal>
	</section>

	<!-- About Preview -->
	<section class="bg-light py-20">
		<ScrollReveal delay={100}>
			<div class="mx-auto max-w-4xl px-4 text-center">
				<span class="inline-block rounded-full bg-gold/10 px-4 py-1.5 text-sm font-medium text-gold">
					Founded in November 1929
				</span>
				<h2 class="mt-6 font-heading text-3xl font-bold text-dark">About PICPA</h2>
				<p class="mt-4 leading-relaxed text-body">
					The Philippine Institute of Certified Public Accountants (PICPA) is the Accredited
					Integrated Professional Organization (AIPO) of CPAs, recognized by the Professional
					Regulation Commission (PRC). For over nine decades, PICPA has been dedicated to promoting,
					upholding, and maintaining high standards in the accountancy profession.
				</p>
				<a
					href="/about"
					class="mt-8 inline-flex items-center gap-2 font-medium text-primary transition-all hover:gap-3"
				>
					Learn More About PICPA &rarr;
				</a>
			</div>
		</ScrollReveal>
	</section>

	<!-- Announcements -->
	<section class="bg-white py-20">
		<div class="mx-auto max-w-7xl px-4">
			<h2 class="text-center font-heading text-3xl font-bold text-dark">Latest Announcements</h2>
			<p class="mt-2 text-center text-body">Stay updated with the latest news from PICPA</p>
			<div class="mt-12 grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
				{#each announcements as item, i (item.title)}
					<ScrollReveal delay={i * 100}>
						<AnnouncementCard
							image={item.image}
							date={item.date}
							title={item.title}
							excerpt={item.excerpt}
						/>
					</ScrollReveal>
				{/each}
			</div>
		</div>
	</section>

	<!-- Foundation Preview -->
	<section class="bg-light py-20">
		<ScrollReveal>
			<div class="mx-auto grid max-w-7xl grid-cols-1 items-center gap-12 px-4 lg:grid-cols-2">
				<div>
					<span class="inline-block rounded-full bg-primary/10 px-4 py-1.5 text-sm font-medium text-primary">
						Established 1981
					</span>
					<h2 class="mt-4 font-heading text-3xl font-bold text-dark">PICPA Foundation Inc.</h2>
					<p class="mt-4 text-body">
						The PICPA Foundation supports the advancement of the accountancy profession through
						research, development, scholarships, and community programs.
					</p>
					<ul class="mt-6 space-y-3">
						{#each programs as program (program)}
							<li class="flex items-center gap-3">
								<svg class="h-5 w-5 shrink-0 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
									<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
								</svg>
								<span class="text-body">{program}</span>
							</li>
						{/each}
					</ul>
					<a href="/foundation" class="mt-6 inline-flex items-center gap-2 font-medium text-primary transition-all hover:gap-3">
						Learn More &rarr;
					</a>
				</div>
				<div>
					<img
						src="/images/foundation/board.png"
						alt="PICPA Foundation Board"
						class="rounded-2xl shadow-lg"
					/>
				</div>
			</div>
		</ScrollReveal>
	</section>

	<!-- CTA Banner -->
	<section class="relative overflow-hidden bg-gradient-to-r from-primary to-primary-dark py-20">
		<img
			src="/images/logos/emblem.png"
			alt=""
			class="pointer-events-none absolute right-0 top-1/2 h-[400px] w-[400px] -translate-y-1/2 translate-x-1/4 opacity-10"
		/>
		<ScrollReveal>
			<div class="relative z-10 mx-auto max-w-4xl px-4 text-center">
				<h2 class="font-heading text-3xl font-bold text-white lg:text-4xl">
					Join the Premier Organization of CPAs in the Philippines
				</h2>
				<p class="mx-auto mt-4 max-w-2xl text-white/80">
					Become part of a community of over 26,000 active members dedicated to excellence in the
					accountancy profession.
				</p>
				<a
					href="/members"
					class="mt-8 inline-block rounded-lg bg-white px-8 py-3.5 font-medium text-primary transition hover:bg-light"
				>
					Become a Member
				</a>
			</div>
		</ScrollReveal>
	</section>
</div>
