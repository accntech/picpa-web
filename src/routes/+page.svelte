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
	<section class="relative flex justify-center items-center bg-primary-deep min-h-screen overflow-hidden">
		<div class="absolute inset-0">
			<iframe
				src="https://www.youtube.com/embed/ir1c7gbSwGw?autoplay=1&mute=1&loop=1&playlist=ir1c7gbSwGw&controls=0&showinfo=0&rel=0&modestbranding=1&playsinline=1"
				title="PICPA Background Video"
				frameborder="0"
				allow="autoplay; encrypted-media"
				allowfullscreen
				class="hero-video pointer-events-none"
			></iframe>
		</div>
		<div class="absolute inset-0 bg-black/60"></div>
		<div class="z-10 relative px-4 text-center">
			<p class="font-medium text-gold text-sm uppercase tracking-widest">EST. 1929</p>
			<h1 class="mx-auto mt-4 max-w-4xl font-heading font-bold text-white text-5xl lg:text-7xl leading-tight">
				Philippine Institute of Certified Public Accountants
			</h1>
			<p class="mx-auto mt-6 max-w-2xl text-white/80 text-lg lg:text-xl">
				The National Organization of Certified Public Accountants
			</p>
			<p class="mt-4 font-medium text-gold">
				Awarded five times as PRC's most outstanding AIPO
			</p>
			<div class="flex justify-center gap-4 mt-10">
				<a
					href="https://picpasystem.com.ph/portal/login.html" target="_blank" rel="noopener noreferrer"
					class="bg-primary hover:bg-primary-dark px-8 py-3.5 rounded-lg font-medium text-white transition"
				>
					My MELS Account
				</a>
				<a
					href="/about"
					class="hover:bg-white px-8 py-3.5 border-2 border-white rounded-lg font-medium text-white hover:text-dark transition"
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
			<div class="items-center gap-12 grid grid-cols-1 lg:grid-cols-2 mx-auto px-4 max-w-7xl">
				<div class="relative">
					<div class="-right-4 -bottom-4 -z-10 absolute bg-primary/20 rounded-2xl w-full h-full"></div>
					<img
						src="/images/president/gbs1.png"
						alt="Gerard B. Sanvictores"
						class="relative border-4 border-primary/20 rounded-2xl object-cover"
					/>
				</div>
				<div>
					<span class="inline-block bg-primary/10 px-4 py-1.5 rounded-full font-medium text-primary text-sm">
						FY 2025-2026
					</span>
					<h2 class="mt-4 font-heading font-bold text-dark text-3xl">Gerard B. Sanvictores</h2>
					<p class="mt-1 text-body">National President</p>
					<p class="mt-6 font-heading font-bold text-primary-dark text-2xl">ACTION with IMPACT</p>
					<div class="gap-6 grid grid-cols-2 mt-8">
						<div class="space-y-2">
							{#each actionWords as word (word)}
								<div class="flex items-center gap-2">
									<span class="bg-primary rounded-full w-2 h-2"></span>
									<span class="text-body">{word}</span>
								</div>
							{/each}
						</div>
						<div class="space-y-2">
							{#each impactWords as word (word)}
								<div class="flex items-center gap-2">
									<span class="bg-primary rounded-full w-2 h-2"></span>
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
			<div class="mx-auto px-4 max-w-4xl text-center">
				<span class="inline-block bg-gold/10 px-4 py-1.5 rounded-full font-medium text-gold text-sm">
					Founded in November 1929
				</span>
				<h2 class="mt-6 font-heading font-bold text-dark text-3xl">About PICPA</h2>
				<p class="mt-4 text-body leading-relaxed">
					The Philippine Institute of Certified Public Accountants (PICPA) is the Accredited
					Integrated Professional Organization (AIPO) of CPAs, recognized by the Professional
					Regulation Commission (PRC). For over nine decades, PICPA has been dedicated to promoting,
					upholding, and maintaining high standards in the accountancy profession.
				</p>
				<a
					href="/about"
					class="inline-flex items-center gap-2 hover:gap-3 mt-8 font-medium text-primary transition-all"
				>
					Learn More About PICPA &rarr;
				</a>
			</div>
		</ScrollReveal>
	</section>

	<!-- Announcements -->
	<section class="bg-white py-20">
		<div class="mx-auto px-4 max-w-7xl">
			<h2 class="font-heading font-bold text-dark text-3xl text-center">Latest Announcements</h2>
			<p class="mt-2 text-body text-center">Stay updated with the latest news from PICPA</p>
			<div class="gap-8 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 mt-12">
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
			<div class="items-center gap-12 grid grid-cols-1 lg:grid-cols-2 mx-auto px-4 max-w-7xl">
				<div>
					<span class="inline-block bg-primary/10 px-4 py-1.5 rounded-full font-medium text-primary text-sm">
						Established 1981
					</span>
					<h2 class="mt-4 font-heading font-bold text-dark text-3xl">PICPA Foundation Inc.</h2>
					<p class="mt-4 text-body">
						The PICPA Foundation supports the advancement of the accountancy profession through
						research, development, scholarships, and community programs.
					</p>
					<ul class="space-y-3 mt-6">
						{#each programs as program (program)}
							<li class="flex items-center gap-3">
								<svg class="w-5 h-5 text-primary shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
									<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
								</svg>
								<span class="text-body">{program}</span>
							</li>
						{/each}
					</ul>
					<a href="/foundation" class="inline-flex items-center gap-2 hover:gap-3 mt-6 font-medium text-primary transition-all">
						Learn More &rarr;
					</a>
				</div>
				<div>
					<img
						src="/images/foundation/board.png"
						alt="PICPA Foundation Board"
						class="shadow-lg rounded-2xl"
					/>
				</div>
			</div>
		</ScrollReveal>
	</section>

	<!-- CTA Banner -->
	<section class="relative bg-linear-to-r from-primary to-primary-dark py-20 overflow-hidden">
		<img
			src="/images/logos/emblem.png"
			alt=""
			class="top-1/2 right-0 absolute opacity-10 w-100 h-100 -translate-y-1/2 translate-x-1/4 pointer-events-none"
		/>
		<ScrollReveal>
			<div class="z-10 relative mx-auto px-4 max-w-4xl text-center">
				<h2 class="font-heading font-bold text-white text-3xl lg:text-4xl">
					Join the Premier Organization of CPAs in the Philippines
				</h2>
				<p class="mx-auto mt-4 max-w-2xl text-white/80">
					Become part of a community of over 26,000 active members dedicated to excellence in the
					accountancy profession.
				</p>
				<a
					href="https://picpasystem.com.ph/portal/login.html" target="_blank" rel="noopener noreferrer"
					class="inline-block bg-white hover:bg-light mt-8 px-8 py-3.5 rounded-lg font-medium text-primary transition"
				>
					My MELS Account
				</a>
			</div>
		</ScrollReveal>
	</section>
</div>

<style>
	.hero-video {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		width: 177.78vh;
		height: 100vh;
		min-width: 100%;
		min-height: 56.25vw;
		border: 0;
	}
</style>
