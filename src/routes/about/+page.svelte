<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';

	const milestones = [
		{
			date: 'November 1929',
			text: 'PICPA was founded by eleven visionary CPAs: Enrique Caguiat, Santiago de la Cruz, Francisco Dalupan, Jaime Hernandez, Felipe Ollada, Ramon del Rosario, Antonio Sanchez, Jose Torres, Artemio Tulio, Clemente Uson, and Jesus Zulueta. W. W. Larkin, CPA Certificate No. 1, served as the first President.'
		},
		{
			date: '1973',
			text: 'Presidential Decree No. 223 officially recognized PICPA as the Accredited Integrated Professional Organization (AIPO) of Certified Public Accountants in the Philippines.'
		},
		{
			date: '2004',
			text: 'Republic Act No. 9298, the Philippine Accountancy Act of 2004, was enacted, further strengthening the regulatory framework for the accountancy profession.'
		},
		{
			date: 'Present',
			text: 'Today, PICPA represents over 196,000 CPAs with more than 26,000 active members, 84 local chapters, and 17 international chapters. PICPA has been awarded five times as PRC\'s most outstanding AIPO.'
		}
	];

	const goals = [
		{
			title: 'Regulate the Practice',
			desc: 'To regulate the practice of the accountancy profession in the Philippines'
		},
		{
			title: 'Advance Knowledge',
			desc: 'To advance the science of accountancy and promote higher professional standards'
		},
		{
			title: 'Foster Collegiality',
			desc: 'To promote and maintain high professional and ethical standards among CPAs'
		},
		{
			title: 'Serve the Public',
			desc: 'To safeguard the interests of the public from unreliable financial reporting'
		}
	];

	const goalIcons = [
		'M9 12h3.75M9 15h3.75M9 18h3.75m3 .75H18a2.25 2.25 0 0 0 2.25-2.25V6.108c0-1.135-.845-2.098-1.976-2.192a48.424 48.424 0 0 0-1.123-.08m-5.801 0c-.065.21-.1.433-.1.664 0 .414.336.75.75.75h4.5a.75.75 0 0 0 .75-.75 2.25 2.25 0 0 0-.1-.664m-5.8 0A2.251 2.251 0 0 1 13.5 2.25H15a2.251 2.251 0 0 1 2.15 1.586m-5.8 0c-.376.023-.75.05-1.124.08C9.095 4.01 8.25 4.973 8.25 6.108V8.25m0 0H4.875c-.621 0-1.125.504-1.125 1.125v11.25c0 .621.504 1.125 1.125 1.125h9.75c.621 0 1.125-.504 1.125-1.125V9.375c0-.621-.504-1.125-1.125-1.125H8.25Z',
		'M12 6.042A8.967 8.967 0 0 0 6 3.75c-1.052 0-2.062.18-3 .512v14.25A8.987 8.987 0 0 1 6 18c2.305 0 4.408.867 6 2.292m0-14.25a8.966 8.966 0 0 1 6-2.292c1.052 0 2.062.18 3 .512v14.25A8.987 8.987 0 0 0 18 18a8.967 8.967 0 0 0-6 2.292m0-14.25v14.25',
		'M15 19.128a9.38 9.38 0 0 0 2.625.372 9.337 9.337 0 0 0 4.121-.952 4.125 4.125 0 0 0-7.533-2.493M15 19.128v-.003c0-1.113-.285-2.16-.786-3.07M15 19.128v.106A12.318 12.318 0 0 1 8.624 21c-2.331 0-4.512-.645-6.374-1.766l-.001-.109a6.375 6.375 0 0 1 11.964-3.07M12 6.375a3.375 3.375 0 1 1-6.75 0 3.375 3.375 0 0 1 6.75 0Zm8.25 2.25a2.625 2.625 0 1 1-5.25 0 2.625 2.625 0 0 1 5.25 0Z',
		'M12 21a9.004 9.004 0 0 0 8.716-6.747M12 21a9.004 9.004 0 0 1-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 0 1 7.843 4.582M12 3a8.997 8.997 0 0 0-7.843 4.582m15.686 0A11.953 11.953 0 0 1 12 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0 1 21 12c0 .778-.099 1.533-.284 2.253m0 0A17.919 17.919 0 0 1 12 16.5c-3.162 0-6.133-.815-8.716-2.247m0 0A9.015 9.015 0 0 1 3 12c0-1.605.42-3.113 1.157-4.418'
	];

	const sectors = [
		{
			acronym: 'ACPAPP',
			title: 'Public Practice',
			desc: 'CPAs providing audit, tax, and advisory services to clients'
		},
		{
			acronym: 'ACPACI',
			title: 'Commerce & Industry',
			desc: 'CPAs employed in private businesses and corporations'
		},
		{
			acronym: 'nACPAE',
			title: 'Education/Academe',
			desc: 'CPAs in academic institutions and accounting education'
		},
		{
			acronym: 'GACPA',
			title: 'Government',
			desc: 'CPAs serving in government agencies and institutions'
		}
	];

	const stats = [
		{ number: 9, label: 'Regions Nationwide' },
		{ number: 21, label: 'Board Members' },
		{ number: 84, label: 'Local Chapters' }
	];

	let counters = $state(stats.map(() => 0));
	let statsVisible = $state(false);

	function animateCounters() {
		if (statsVisible) return;
		statsVisible = true;
		stats.forEach((stat, i) => {
			const target = stat.number;
			const duration = 1500;
			const steps = 40;
			const increment = target / steps;
			let current = 0;
			const interval = setInterval(() => {
				current += increment;
				if (current >= target) {
					counters[i] = target;
					clearInterval(interval);
				} else {
					counters[i] = Math.floor(current);
				}
			}, duration / steps);
		});
	}

	function observeStats(node: HTMLElement) {
		const observer = new IntersectionObserver(
			([entry]) => {
				if (entry.isIntersecting) {
					animateCounters();
					observer.disconnect();
				}
			},
			{ threshold: 0.3 }
		);
		observer.observe(node);
		return { destroy: () => observer.disconnect() };
	}
</script>

<PageHero title="About PICPA" breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'About' }]} />

<section class="bg-white py-24">
	<div class="mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="max-w-2xl">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Our Heritage</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold leading-tight text-dark">
					A Legacy of Professional Excellence
				</h2>
				<p class="mt-4 leading-relaxed text-body">
					From humble beginnings to the premier CPA organization in the Philippines
				</p>
			</div>
		</ScrollReveal>

		<div class="mt-16 hidden lg:block">
			<div class="relative">
				<div class="absolute top-6 left-0 right-0 h-0.5 bg-linear-to-r from-primary/20 via-primary to-primary/20"></div>
				<div class="absolute top-3 left-1/2 -translate-x-1/2">
					<svg class="h-7 w-12 text-primary/30" viewBox="0 0 87 85" fill="currentColor">
						<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
						<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
						<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
						<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
					</svg>
				</div>
				<div class="grid grid-cols-4 gap-8">
					{#each milestones as milestone, i (milestone.date)}
						<ScrollReveal delay={i * 120}>
							<div class="pt-14">
								<div class="absolute -mt-8 h-3 w-3 rounded-full border-[3px] border-white bg-primary shadow-sm" style="animation: pulse-glow 3s ease-in-out infinite {i * 0.5}s;"></div>
								<p class="text-sm font-bold tracking-wide text-primary">{milestone.date}</p>
								<p class="mt-3 text-sm leading-relaxed text-body">{milestone.text}</p>
							</div>
						</ScrollReveal>
					{/each}
				</div>
			</div>
		</div>

		<div class="mt-12 lg:hidden">
			<div class="relative ml-4 border-l-2 border-primary/30">
				{#each milestones as milestone, i (milestone.date)}
					<ScrollReveal delay={i * 80}>
						<div class="relative pb-10 pl-8">
							<div class="absolute left-[-9px] top-0.5 h-4 w-4 rounded-full border-[3px] border-white bg-primary shadow-sm"></div>
							<p class="text-sm font-bold tracking-wide text-primary">{milestone.date}</p>
							<p class="mt-2 leading-relaxed text-body">{milestone.text}</p>
						</div>
					</ScrollReveal>
				{/each}
			</div>
		</div>
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
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Our Purpose</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">
					Founding Goals
				</h2>
			</div>
		</ScrollReveal>

		<div class="mt-14 grid grid-cols-1 gap-6 md:grid-cols-2">
			{#each goals as goal, i (goal.title)}
				<ScrollReveal stagger={i}>
					<div class="glass rounded-2xl p-8 transition-all duration-300 hover:-translate-y-1 hover:border-primary/20">
						<div class="flex h-12 w-12 items-center justify-center rounded-xl bg-primary/10">
							<svg class="h-6 w-6 text-primary" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
								<path stroke-linecap="round" stroke-linejoin="round" d={goalIcons[i]} />
							</svg>
						</div>
						<h3 class="mt-5 font-heading text-xl font-bold text-white">{goal.title}</h3>
						<p class="mt-2 leading-relaxed text-slate">{goal.desc}</p>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="max-w-2xl">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Organization</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold leading-tight text-dark">
					Four Professional Sectors
				</h2>
				<p class="mt-4 leading-relaxed text-body">
					PICPA members are organized into four key sectors of the profession
				</p>
			</div>
		</ScrollReveal>

		<div class="mt-14 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-4">
			{#each sectors as sector, i (sector.acronym)}
				<ScrollReveal stagger={i}>
					<div class="rounded-2xl border-l-4 border-primary bg-white p-6 shadow-sm transition-all duration-300 hover:-translate-y-1 hover:shadow-lg">
						<p class="text-xs font-bold uppercase tracking-wider text-primary">
							{sector.acronym}
						</p>
						<h3 class="mt-3 font-heading text-lg font-bold text-dark">{sector.title}</h3>
						<p class="mt-2 text-sm leading-relaxed text-body">{sector.desc}</p>
						<div class="mt-4 flex items-center gap-1 text-sm font-medium text-primary">
							<span>Learn more</span>
							<svg class="h-4 w-4" viewBox="0 0 20 20" fill="none" stroke="currentColor" stroke-width="2">
								<polyline points="6,4 14,10 6,16" />
								<polyline points="10,4 18,10 10,16" />
							</svg>
						</div>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="relative bg-navy py-24">
	<div class="gradient-mesh-bg absolute inset-0"></div>

	<div class="relative mx-auto max-w-4xl px-4 lg:px-8" use:observeStats>
		<ScrollReveal>
			<div class="text-center">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">By the Numbers</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">
					Organizational Structure
				</h2>
			</div>
		</ScrollReveal>

		<div class="mt-14 grid grid-cols-3 gap-8">
			{#each stats as stat, i (stat.label)}
				<ScrollReveal stagger={i}>
					<div class="glass rounded-2xl p-8 text-center">
						<p class="font-heading text-[clamp(2rem,4vw,3.5rem)] font-bold text-primary">
							{counters[i]}
						</p>
						<p class="mt-2 text-sm font-medium text-slate">{stat.label}</p>
					</div>
				</ScrollReveal>
			{/each}
		</div>

		<ScrollReveal delay={300}>
			<p class="mx-auto mt-12 max-w-2xl text-center leading-relaxed text-slate">
				PICPA's organizational structure spans 9 regions across the Philippines, governed by a
				21-member National Board of Directors, with 84 local chapters and 17 international
				chapters ensuring representation for all Filipino CPAs worldwide.
			</p>
		</ScrollReveal>
	</div>
</section>
