<script lang="ts">
	import StatsBar from '$lib/components/stats-bar.svelte';
	import AnnouncementCard from '$lib/components/announcement-card.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';

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

	const programs = [
		'Research & Development',
		'Professional Development',
		'Scholarships',
		'Ayuda sa Escuela'
	];
</script>

<div class="pt-0">
	<section class="relative flex items-center bg-navy min-h-screen overflow-hidden">
		<div class="absolute inset-0">
			<iframe
				src="https://www.youtube.com/embed/ir1c7gbSwGw?autoplay=1&mute=1&loop=1&playlist=ir1c7gbSwGw&controls=0&showinfo=0&rel=0&modestbranding=1&playsinline=1"
				title="PICPA Background Video"
				frameborder="0"
				allow="autoplay; encrypted-media"
				allowfullscreen
				class="pointer-events-none hero-video"
			></iframe>
		</div>

		<div class="absolute inset-0 bg-linear-to-b from-navy/80 via-navy/60 to-navy/90"></div>

		<div
			class="-top-32 -left-32 absolute opacity-30 rounded-full w-125 h-125"
			style="background: radial-gradient(circle, rgba(24,179,85,0.2) 0%, transparent 70%);"
		></div>
		<div
			class="-right-24 -bottom-24 absolute opacity-20 rounded-full w-100 h-100"
			style="background: radial-gradient(circle, rgba(99,102,241,0.15) 0%, transparent 70%);"
		></div>
		<div
			class="top-1/3 right-1/4 absolute opacity-15 rounded-full w-75 h-75"
			style="background: radial-gradient(circle, rgba(212,168,67,0.12) 0%, transparent 70%);"
		></div>

		<svg
			class="-top-8 -right-12 absolute w-72 h-72 text-white/3"
			style="animation: float 6s ease-in-out infinite;"
			viewBox="0 0 87 85"
			fill="currentColor"
		>
			<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
			<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
			<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
			<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
		</svg>
		<svg
			class="-bottom-10 -left-8 absolute w-56 h-56 text-white/3"
			style="animation: float-reverse 7s ease-in-out infinite;"
			viewBox="0 0 87 85"
			fill="currentColor"
		>
			<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
			<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
			<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
			<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
		</svg>
		<svg
			class="top-1/2 left-1/3 absolute w-24 h-24 text-white/2"
			style="animation: float 8s ease-in-out infinite 1s;"
			viewBox="0 0 87 85"
			fill="currentColor"
		>
			<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
			<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
			<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
			<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
		</svg>

		<div class="z-10 relative mx-auto px-4 lg:px-8 py-32 w-full max-w-7xl">
			<div class="flex lg:flex-row flex-col lg:justify-between items-start lg:items-end gap-12">
				<div class="max-w-3xl">
					<h1
						class="mt-6 font-heading font-bold text-[clamp(2.5rem,5vw,5rem)] text-white leading-[1.1] tracking-tight"
					>
						Philippine Institute of Certified Public Accountants
					</h1>
					<p class="mt-6 max-w-xl text-slate text-lg lg:text-xl">
						The National Organization of Certified Public Accountants
					</p>
					<p class="mt-3 font-medium text-gold/80">
						Awarded five times as PRC's most outstanding AIPO
					</p>
				</div>
				<div class="flex sm:flex-row flex-col gap-3 shrink-0">
					<a
						href="https://picpasystem.com.ph/portal/login.html"
						target="_blank"
						rel="noopener noreferrer"
						class="bg-primary hover:bg-primary-dark hover:shadow-[0_0_30px_rgba(24,179,85,0.3)] px-8 py-3.5 rounded-lg font-medium text-white text-center transition-all duration-300"
					>
						My MELS Account
					</a>
					<a
						href="/about"
						class="hover:bg-white px-8 py-3.5 border-2 border-white/20 hover:border-white rounded-lg font-medium text-white hover:text-dark text-center transition-all duration-300"
					>
						Learn More
					</a>
				</div>
			</div>
		</div>

		<div class="bottom-8 left-1/2 z-10 absolute -translate-x-1/2">
			<svg
				class="w-6 h-6 text-white/50 animate-[chevron-bounce_2s_ease-in-out_infinite]"
				fill="none"
				viewBox="0 0 24 24"
				stroke="currentColor"
				stroke-width="2"
			>
				<polyline points="6,9 12,15 18,9" />
			</svg>
		</div>
	</section>

	<StatsBar />

	<section class="bg-white py-24 overflow-hidden">
		<div class="mx-auto px-4 lg:px-8 max-w-7xl">
			<div class="items-center gap-0 grid grid-cols-1 lg:grid-cols-[45fr_55fr]">
				<ScrollReveal direction="left">
					<div class="relative">
						<img
							src="/images/president/gbs1.png"
							alt="Gerard B. Sanvictores"
							class="relative rounded-2xl w-full h-full object-cover"
						/>
						<div
							class="hidden lg:block right-0 absolute inset-y-0 bg-linear-to-r from-transparent to-white w-24"
						></div>
						<span
							class="-bottom-4 left-8 absolute px-5 py-2 rounded-full font-medium text-white text-sm glass"
						>
							FY 2025-2026
						</span>
					</div>
				</ScrollReveal>
				<div class="mt-12 lg:mt-0 lg:pl-12">
					<ScrollReveal direction="right">
						<h2 class="font-heading font-bold text-dark text-3xl lg:text-4xl">
							Gerard B. Sanvictores
						</h2>
						<p class="mt-1 text-body">National President</p>
						<p class="mt-6 font-heading font-bold text-primary-dark text-2xl">
							ACTION with IMPACT
						</p>
					</ScrollReveal>
					<div class="gap-x-8 gap-y-0 grid grid-cols-2 mt-8">
						<div>
							{#each actionWords as word, i (word)}
								<ScrollReveal stagger={i}>
									<div class="flex items-center gap-3 py-1.5">
										<svg
											class="w-4 h-4 text-primary shrink-0"
											viewBox="0 0 24 24"
											fill="none"
											stroke="currentColor"
											stroke-width="2.5"
										>
											<polyline points="9,6 15,12 9,18" />
											<polyline points="15,6 21,12 15,18" />
										</svg>
										<span class="text-body">{word}</span>
									</div>
								</ScrollReveal>
							{/each}
						</div>
						<div>
							{#each impactWords as word, i (word)}
								<ScrollReveal stagger={i}>
									<div class="flex items-center gap-3 py-1.5">
										<svg
											class="w-4 h-4 text-primary shrink-0"
											viewBox="0 0 24 24"
											fill="none"
											stroke="currentColor"
											stroke-width="2.5"
										>
											<polyline points="9,6 15,12 9,18" />
											<polyline points="15,6 21,12 15,18" />
										</svg>
										<span class="text-body">{word}</span>
									</div>
								</ScrollReveal>
							{/each}
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<section
		class="bg-light py-24"
		style="clip-path: polygon(0 5%, 100% 0, 100% 100%, 0 100%);"
	>
		<ScrollReveal delay={100}>
			<div class="mx-auto px-4 lg:px-8 pt-8 max-w-4xl">
				<span
					class="inline-block bg-gold/10 px-4 py-1.5 border border-gold/30 rounded-full font-medium text-gold text-xs uppercase tracking-widest"
				>
					Founded in November 1929
				</span>
				<h2 class="mt-6 font-heading font-bold text-dark text-3xl">About PICPA</h2>
				<p
					class="mt-6 font-heading text-[clamp(1.25rem,2.5vw,1.75rem)] text-body leading-relaxed"
				>
					The Philippine Institute of Certified Public Accountants (PICPA) is the Accredited
					Integrated Professional Organization (AIPO) of CPAs, recognized by the Professional
					Regulation Commission (PRC). For over nine decades, PICPA has been dedicated to
					promoting, upholding, and maintaining high standards in the accountancy profession.
				</p>
				<a
					href="/about"
					class="group inline-flex items-center gap-2 mt-8 font-medium text-primary transition-all"
				>
					Learn More About PICPA
					<svg
						class="w-5 h-5 transition-transform group-hover:translate-x-1.5 duration-300"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						stroke-width="2"
					>
						<path stroke-linecap="round" stroke-linejoin="round" d="M17 8l4 4m0 0l-4 4m4-4H3" />
					</svg>
				</a>
			</div>
		</ScrollReveal>
	</section>

	<section class="bg-white py-32">
		<div class="mx-auto px-4 lg:px-8 max-w-7xl">
			<ScrollReveal>
				<div class="text-center">
					<h2 class="font-heading font-bold text-dark text-3xl lg:text-4xl">
						Latest Announcements
					</h2>
					<p class="mt-2 text-body">Stay updated with the latest news from PICPA</p>
				</div>
			</ScrollReveal>

			<div class="hidden gap-6 lg:grid lg:grid-cols-3 lg:grid-rows-2 mt-12">
				{#each announcements as item, i (item.title)}
					<ScrollReveal delay={i * 80} stagger={0}>
						<div class={i === 0 ? 'row-span-2 h-full [&>article]:h-full' : ''}>
							<AnnouncementCard
								image={item.image}
								date={item.date}
								title={item.title}
								excerpt={item.excerpt}
							/>
						</div>
					</ScrollReveal>
				{/each}
			</div>

			<div
				class="lg:hidden flex gap-4 mt-12 pb-4 overflow-x-auto snap-mandatory snap-x"
				style="-webkit-overflow-scrolling: touch;"
			>
				{#each announcements as item, i (item.title)}
					<div class="min-w-[80vw] snap-center shrink-0">
						<ScrollReveal delay={i * 80}>
							<AnnouncementCard
								image={item.image}
								date={item.date}
								title={item.title}
								excerpt={item.excerpt}
							/>
						</ScrollReveal>
					</div>
				{/each}
			</div>
		</div>
	</section>

	<section class="relative bg-navy py-32 overflow-hidden">
		<div class="absolute inset-0 gradient-mesh-bg"></div>
		<div class="z-10 relative mx-auto px-4 lg:px-8 max-w-7xl">
			<div class="items-center gap-12 grid grid-cols-1 lg:grid-cols-2">
				<div>
					<ScrollReveal direction="left">
						<span
							class="inline-block bg-primary/10 px-4 py-1.5 border border-primary/30 rounded-full font-medium text-primary text-xs uppercase tracking-widest"
						>
							Established 1981
						</span>
						<h2 class="mt-6 font-heading font-bold text-white text-3xl lg:text-4xl">
							PICPA Foundation Inc.
						</h2>
						<p class="mt-4 text-slate text-lg">
							The PICPA Foundation supports the advancement of the accountancy profession
							through research, development, scholarships, and community programs.
						</p>
						<ul class="space-y-4 mt-8">
							{#each programs as program (program)}
								<li class="flex items-center gap-3">
									<svg
										class="w-5 h-5 text-primary shrink-0"
										viewBox="0 0 24 24"
										fill="none"
										stroke="currentColor"
										stroke-width="2.5"
									>
										<polyline points="9,6 15,12 9,18" />
										<polyline points="15,6 21,12 15,18" />
									</svg>
									<span class="text-slate">{program}</span>
								</li>
							{/each}
						</ul>
						<a
							href="/foundation"
							class="group inline-flex items-center gap-2 mt-8 font-medium text-primary transition-all"
						>
							Learn More
							<svg
								class="w-5 h-5 transition-transform group-hover:translate-x-1.5 duration-300"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor"
								stroke-width="2"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									d="M17 8l4 4m0 0l-4 4m4-4H3"
								/>
							</svg>
						</a>
					</ScrollReveal>
				</div>
				<ScrollReveal direction="right">
					<div class="relative lg:-mr-8">
						<img
							src="/images/foundation/board.png"
							alt="PICPA Foundation Board"
							class="relative shadow-2xl rounded-2xl"
						/>
						<div class="hidden lg:block -bottom-12 -left-28 absolute p-6 rounded-2xl glass">
							<p class="font-heading font-bold text-white text-2xl">40+</p>
							<p class="mt-1 text-slate text-sm">Years of Service</p>
						</div>
					</div>
				</ScrollReveal>
			</div>
		</div>
	</section>

	<section class="relative bg-navy py-24 overflow-hidden">
		<div class="absolute inset-0 gradient-mesh-bg"></div>

		<svg
			class="-top-6 -left-8 absolute w-64 h-64 text-white/3"
			style="animation: float 7s ease-in-out infinite;"
			viewBox="0 0 87 85"
			fill="currentColor"
		>
			<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
			<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
			<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
			<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
		</svg>
		<svg
			class="-right-8 -bottom-6 absolute w-48 h-48 text-white/3"
			style="animation: float-reverse 6s ease-in-out infinite;"
			viewBox="0 0 87 85"
			fill="currentColor"
		>
			<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
			<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
			<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
			<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
		</svg>

		<ScrollReveal>
			<div class="z-10 relative mx-auto px-4 lg:px-8 max-w-4xl text-center">
				<h2 class="font-heading font-bold text-white text-3xl lg:text-4xl">
					Join the Premier Organization of CPAs in the Philippines
				</h2>
				<p class="mx-auto mt-4 max-w-2xl text-slate">
					Become part of a community of over 26,000 active members dedicated to excellence
					in the accountancy profession.
				</p>
				<a
					href="https://picpasystem.com.ph/portal/login.html"
					target="_blank"
					rel="noopener noreferrer"
					class="inline-block bg-primary hover:bg-primary-dark hover:shadow-[0_0_30px_rgba(24,179,85,0.4)] mt-8 px-10 py-4 rounded-lg font-medium text-white transition-all duration-300"
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
