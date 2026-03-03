<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';

	const coreValues = [
		{
			title: 'Professional Excellence',
			desc: 'Dedication to excellence across all areas of professional practice',
			icon: 'M11.48 3.499a.562.562 0 0 1 1.04 0l2.125 5.111a.563.563 0 0 0 .475.345l5.518.442c.499.04.701.663.321.988l-4.204 3.602a.563.563 0 0 0-.182.557l1.285 5.385a.562.562 0 0 1-.84.61l-4.725-2.885a.562.562 0 0 0-.586 0L6.982 20.54a.562.562 0 0 1-.84-.61l1.285-5.386a.562.562 0 0 0-.182-.557l-4.204-3.602a.562.562 0 0 1 .321-.988l5.518-.442a.563.563 0 0 0 .475-.345L11.48 3.5Z'
		},
		{
			title: 'Integrity',
			desc: 'Truthfulness, honesty, uprightness, and sound moral principles',
			icon: 'M9 12.75 11.25 15 15 9.75m-3-7.036A11.959 11.959 0 0 1 3.598 6 11.99 11.99 0 0 0 3 9.749c0 5.592 3.824 10.29 9 11.623 5.176-1.332 9-6.03 9-11.622 0-1.31-.21-2.571-.598-3.751h-.152c-3.196 0-6.1-1.248-8.25-3.285Z'
		},
		{
			title: 'Commitment',
			desc: 'Dedication to organizational ideals and PICPA objectives',
			icon: 'M15.362 5.214A8.252 8.252 0 0 1 12 21 8.25 8.25 0 0 1 6.038 7.047 8.287 8.287 0 0 0 9 9.601a8.983 8.983 0 0 1 3.361-6.867 8.21 8.21 0 0 0 3 2.48Z'
		},
		{
			title: 'Partnership & Team Work',
			desc: 'Unity, harmony, and collaborative spirit among members',
			icon: 'M15 19.128a9.38 9.38 0 0 0 2.625.372 9.337 9.337 0 0 0 4.121-.952 4.125 4.125 0 0 0-7.533-2.493M15 19.128v-.003c0-1.113-.285-2.16-.786-3.07M15 19.128v.106A12.318 12.318 0 0 1 8.624 21c-2.331 0-4.512-.645-6.374-1.766l-.001-.109a6.375 6.375 0 0 1 11.964-3.07M12 6.375a3.375 3.375 0 1 1-6.75 0 3.375 3.375 0 0 1 6.75 0Zm8.25 2.25a2.625 2.625 0 1 1-5.25 0 2.625 2.625 0 0 1 5.25 0Z'
		},
		{
			title: 'Advocacy for Quality',
			desc: 'Strict adherence to the code of professional conduct',
			icon: 'M9 12.75 11.25 15 15 9.75M21 12c0 1.268-.63 2.39-1.593 3.068a3.745 3.745 0 0 1-1.043 3.296 3.745 3.745 0 0 1-3.296 1.043A3.745 3.745 0 0 1 12 21c-1.268 0-2.39-.63-3.068-1.593a3.746 3.746 0 0 1-3.296-1.043 3.745 3.745 0 0 1-1.043-3.296A3.745 3.745 0 0 1 3 12c0-1.268.63-2.39 1.593-3.068a3.745 3.745 0 0 1 1.043-3.296 3.746 3.746 0 0 1 3.296-1.043A3.746 3.746 0 0 1 12 3c1.268 0 2.39.63 3.068 1.593a3.746 3.746 0 0 1 3.296 1.043 3.745 3.745 0 0 1 1.043 3.296A3.745 3.745 0 0 1 21 12Z'
		},
		{
			title: 'New Technologies & Innovativeness',
			desc: 'Continuous pursuit of creativity and technological advancement',
			icon: 'M12 18v-5.25m0 0a6.01 6.01 0 0 0 1.5-.189m-1.5.189a6.01 6.01 0 0 1-1.5-.189m3.75 7.478a12.06 12.06 0 0 1-4.5 0m3.75 2.383a14.406 14.406 0 0 1-3 0M14.25 18v-.192c0-.983.658-1.823 1.508-2.316a7.5 7.5 0 1 0-7.517 0c.85.493 1.509 1.333 1.509 2.316V18'
		},
		{
			title: 'Social Responsibility',
			desc: 'Active commitment to societal duty and community service',
			icon: 'M12 21a9.004 9.004 0 0 0 8.716-6.747M12 21a9.004 9.004 0 0 1-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 0 1 7.843 4.582M12 3a8.997 8.997 0 0 0-7.843 4.582m15.686 0A11.953 11.953 0 0 1 12 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0 1 21 12c0 .778-.099 1.533-.284 2.253m0 0A17.919 17.919 0 0 1 12 16.5c-3.162 0-6.133-.815-8.716-2.247m0 0A9.015 9.015 0 0 1 3 12c0-1.605.42-3.113 1.157-4.418'
		}
	];
</script>

<PageHero
	title="Vision & Mission"
	breadcrumbs={[
		{ label: 'Home', href: '/' },
		{ label: 'About', href: '/about' },
		{ label: 'Vision & Mission' }
	]}
/>

<section class="bg-white py-24">
	<div class="mx-auto max-w-4xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Our Vision</p>
				<div class="mt-8 flex items-start justify-center gap-4">
					<svg class="mt-1 h-10 w-8 shrink-0 text-primary/30" viewBox="0 0 87 85" fill="currentColor">
						<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
						<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
						<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
						<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
					</svg>
					<p class="font-heading text-[clamp(1.25rem,2.5vw,1.75rem)] font-bold leading-relaxed text-dark">
						A responsive and globally relevant professional organization committed to service excellence towards its members and stakeholders.
					</p>
					<svg class="mt-1 h-10 w-8 shrink-0 text-primary/30" viewBox="0 0 87 85" fill="currentColor">
						<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
						<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
						<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
						<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
					</svg>
				</div>
				<div class="mx-auto mt-8 h-1 w-20 rounded-full bg-primary"></div>
			</div>
		</ScrollReveal>
	</div>
</section>

<div class="relative">
	<div class="absolute inset-x-0 top-0 h-24 bg-white"></div>
	<div class="absolute inset-x-0 bottom-0 h-24 bg-light"></div>
	<div class="relative h-12" style="clip-path: polygon(0 0, 100% 0, 100% 100%, 0 40%);">
		<div class="h-full bg-white"></div>
	</div>
	<div class="relative h-12" style="clip-path: polygon(0 0, 100% 60%, 100% 100%, 0 100%);">
		<div class="h-full bg-light"></div>
	</div>
</div>

<section class="bg-light py-24">
	<div class="mx-auto max-w-4xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Our Mission</p>
				<div class="mt-8 flex items-start justify-center gap-4">
					<svg class="mt-1 h-10 w-8 shrink-0 text-primary/30" viewBox="0 0 87 85" fill="currentColor">
						<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
						<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
						<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
						<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
					</svg>
					<p class="font-heading text-[clamp(1.25rem,2.5vw,1.75rem)] font-bold leading-relaxed text-dark">
						To serve the best interest of the members and the stakeholders while promoting, upholding, and maintaining high standards in the accountancy profession and protecting public interest.
					</p>
					<svg class="mt-1 h-10 w-8 shrink-0 text-primary/30" viewBox="0 0 87 85" fill="currentColor">
						<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
						<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
						<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
						<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
					</svg>
				</div>
				<div class="mx-auto mt-8 h-1 w-20 rounded-full bg-primary"></div>
			</div>
		</ScrollReveal>
	</div>
</section>

<div class="relative">
	<div class="absolute inset-x-0 top-0 h-24 bg-light"></div>
	<div class="absolute inset-x-0 bottom-0 h-24 bg-navy"></div>
	<div class="relative h-12" style="clip-path: polygon(0 0, 100% 0, 100% 40%, 0 100%);">
		<div class="h-full bg-light"></div>
	</div>
	<div class="relative h-12" style="clip-path: polygon(0 60%, 100% 0, 100% 100%, 0 100%);">
		<div class="h-full bg-navy"></div>
	</div>
</div>

<section class="relative bg-navy py-24">
	<div class="gradient-mesh-bg absolute inset-0"></div>

	<svg class="absolute bottom-8 right-12 h-32 w-32 text-white/3" style="animation: float-reverse 7s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<p class="text-sm font-medium uppercase tracking-widest text-primary">Our Principles</p>
				<h2 class="mt-3 font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">
					Core Values
				</h2>
				<p class="mt-4 text-slate">The principles that guide our organization</p>
			</div>
		</ScrollReveal>

		<div class="mt-14 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each coreValues as value, i (value.title)}
				<ScrollReveal stagger={i}>
					<div class="glass rounded-2xl p-8 transition-all duration-300 hover:-translate-y-1 hover:border-primary/20">
						<div class="flex h-12 w-12 items-center justify-center rounded-xl bg-primary/10">
							<svg class="h-6 w-6 text-primary" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
								<path stroke-linecap="round" stroke-linejoin="round" d={value.icon} />
							</svg>
						</div>
						<h3 class="mt-5 font-heading text-lg font-bold text-white">{value.title}</h3>
						<p class="mt-2 leading-relaxed text-slate">{value.desc}</p>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>
