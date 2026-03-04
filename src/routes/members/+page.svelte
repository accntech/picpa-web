<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';

	const benefits = [
		{
			icon: 'book',
			title: 'Professional Development',
			desc: 'Access to CPD seminars, workshops, conferences, and the PICPA Academy for continuous learning.'
		},
		{
			icon: 'users',
			title: 'Networking',
			desc: 'Connect with over 26,000 active members across 84 local and 17 international chapters.'
		},
		{
			icon: 'certificate',
			title: 'CPD Credits',
			desc: 'Earn continuing professional development credits required for CPA license renewal.'
		},
		{
			icon: 'briefcase',
			title: 'Career Support',
			desc: 'Free job posting service, career resources, and access to the PICPA careers portal.'
		},
		{
			icon: 'megaphone',
			title: 'Advocacy',
			desc: 'Be part of the voice shaping accountancy regulations and standards in the Philippines.'
		}
	];

	const steps = [
		{
			number: 1,
			title: 'Visit MELS Portal',
			desc: 'Go to picpasystem.com.ph to access the Member Electronic Ledger System'
		},
		{
			number: 2,
			title: 'Create Account',
			desc: 'Register a new account with your email address and personal information'
		},
		{
			number: 3,
			title: 'Fill Application',
			desc: 'Complete the membership application form with your professional details'
		},
		{
			number: 4,
			title: 'Upload Requirements',
			desc: 'Submit required documents including PRC ID and other credentials'
		},
		{
			number: 5,
			title: 'Payment & Confirmation',
			desc: 'Pay the membership fee and receive your confirmation'
		}
	];

	const faqs = [
		{
			question: 'How do I register as a PICPA member?',
			answer: 'Visit the MELS portal at picpasystem.com.ph, create an account, fill out the application form, upload your requirements, and complete the payment process.'
		},
		{
			question: 'What are the requirements for membership?',
			answer: 'You need a valid PRC ID, proof of CPA licensure, and other personal documents. The specific requirements are listed on the MELS registration portal.'
		},
		{
			question: 'How much is the membership fee?',
			answer: 'Membership fees vary by chapter and membership type. Please visit the MELS portal or contact your local chapter for the current fee schedule.'
		},
		{
			question: 'How do I access the MELS system?',
			answer: 'Visit picpasystem.com.ph and log in with your registered credentials. If you\'ve forgotten your password, use the password reset function on the login page.'
		}
	];

	let openFaq = $state<number | null>(null);

	function toggleFaq(index: number) {
		openFaq = openFaq === index ? null : index;
	}
</script>

<PageHero title="Member Services" breadcrumbs={[{label: 'Home', href: '/'}, {label: 'Members'}]} />

<section class="relative overflow-hidden bg-navy py-24">
	<div class="gradient-mesh-bg absolute inset-0"></div>
	<svg class="pointer-events-none absolute -top-10 -right-12 h-80 w-80 text-white/3" style="animation: float 6s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<h2 class="font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">Why Join PICPA?</h2>
			<p class="mt-3 max-w-2xl text-slate">Membership unlocks a full ecosystem of professional growth, networking, and career support for Filipino CPAs.</p>
		</ScrollReveal>

		<div class="mt-14 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each benefits as benefit, i (benefit.title)}
				<ScrollReveal class="h-full" stagger={i}>
					<div class="glass h-full rounded-2xl p-8 transition-all duration-300 hover:-translate-y-0.5 hover:shadow-[0_0_30px_rgba(24,179,85,0.1)]">
						<div class="flex h-12 w-12 items-center justify-center rounded-xl bg-primary/10">
							{#if benefit.icon === 'book'}
								<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M12 6.042A8.967 8.967 0 006 3.75c-1.052 0-2.062.18-3 .512v14.25A8.987 8.987 0 016 18c2.305 0 4.408.867 6 2.292m0-14.25a8.966 8.966 0 016-2.292c1.052 0 2.062.18 3 .512v14.25A8.987 8.987 0 0018 18a8.967 8.967 0 00-6 2.292m0-14.25v14.25" />
								</svg>
							{:else if benefit.icon === 'users'}
								<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M15 19.128a9.38 9.38 0 002.625.372 9.337 9.337 0 004.121-.952 4.125 4.125 0 00-7.533-2.493M15 19.128v-.003c0-1.113-.285-2.16-.786-3.07M15 19.128v.106A12.318 12.318 0 018.624 21c-2.331 0-4.512-.645-6.374-1.766l-.001-.109a6.375 6.375 0 0111.964-3.07M12 6.375a3.375 3.375 0 11-6.75 0 3.375 3.375 0 016.75 0zm8.25 2.25a2.625 2.625 0 11-5.25 0 2.625 2.625 0 015.25 0z" />
								</svg>
							{:else if benefit.icon === 'certificate'}
								<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M9 12.75L11.25 15 15 9.75M21 12c0 1.268-.63 2.39-1.593 3.068a3.745 3.745 0 01-1.043 3.296 3.745 3.745 0 01-3.296 1.043A3.745 3.745 0 0112 21c-1.268 0-2.39-.63-3.068-1.593a3.746 3.746 0 01-3.296-1.043 3.745 3.745 0 01-1.043-3.296A3.745 3.745 0 013 12c0-1.268.63-2.39 1.593-3.068a3.745 3.745 0 011.043-3.296 3.746 3.746 0 013.296-1.043A3.746 3.746 0 0112 3c1.268 0 2.39.63 3.068 1.593a3.746 3.746 0 013.296 1.043 3.746 3.746 0 011.043 3.296A3.745 3.745 0 0121 12z" />
								</svg>
							{:else if benefit.icon === 'briefcase'}
								<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M20.25 14.15v4.25c0 1.094-.787 2.036-1.872 2.18-2.087.277-4.216.42-6.378.42s-4.291-.143-6.378-.42c-1.085-.144-1.872-1.086-1.872-2.18v-4.25m16.5 0a2.18 2.18 0 00.75-1.661V8.706c0-1.081-.768-2.015-1.837-2.175a48.114 48.114 0 00-3.413-.387m4.5 8.006c-.194.165-.42.295-.673.38A23.978 23.978 0 0112 15.75c-2.648 0-5.195-.429-7.577-1.22a2.016 2.016 0 01-.673-.38m0 0A2.18 2.18 0 013 12.489V8.706c0-1.081.768-2.015 1.837-2.175a48.111 48.111 0 013.413-.387m7.5 0V5.25A2.25 2.25 0 0013.5 3h-3a2.25 2.25 0 00-2.25 2.25v.894m7.5 0a48.667 48.667 0 00-7.5 0" />
								</svg>
							{:else}
								<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M10.34 15.84c-.688-.06-1.386-.09-2.09-.09H7.5a4.5 4.5 0 110-9h.75c.704 0 1.402-.03 2.09-.09m0 9.18c.253.962.584 1.892.985 2.783.247.55.06 1.21-.463 1.511l-.657.38c-.551.318-1.26.117-1.527-.461a20.845 20.845 0 01-1.44-4.282m3.102.069a18.03 18.03 0 01-.59-4.59c0-1.586.205-3.124.59-4.59m0 9.18a23.848 23.848 0 018.835 2.535M10.34 6.66a23.847 23.847 0 008.835-2.535m0 0A23.74 23.74 0 0018.795 3m.38 1.125a23.91 23.91 0 011.014 5.395m-1.014 8.855c-.118.38-.245.754-.38 1.125m.38-1.125a23.91 23.91 0 001.014-5.395m0-3.46c.495.413.811 1.035.811 1.73 0 .695-.316 1.317-.811 1.73m0-3.46a24.347 24.347 0 010 3.46" />
								</svg>
							{/if}
						</div>
						<h3 class="mt-5 font-heading text-lg font-bold text-white">{benefit.title}</h3>
						<p class="mt-2 text-sm leading-relaxed text-white/70">{benefit.desc}</p>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="bg-light py-24">
	<div class="mx-auto max-w-4xl px-4 lg:px-8">
		<ScrollReveal>
			<h2 class="font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-dark">How to Register</h2>
			<p class="mt-3 text-body">Follow these 5 simple steps to become a PICPA member</p>
		</ScrollReveal>

		<div class="mt-16 space-y-10">
			{#each steps as step, i (step.number)}
				<ScrollReveal stagger={i}>
					<div class="flex items-start gap-4 sm:gap-8">
						<span class="font-heading text-[clamp(2.5rem,5vw,4.5rem)] leading-none font-bold text-primary/15 select-none">
							{String(step.number).padStart(2, '0')}
						</span>
						<div class="flex-1 border-t border-primary/10 pt-4">
							<h3 class="font-heading text-xl font-bold text-dark">{step.title}</h3>
							<p class="mt-2 max-w-xl leading-relaxed text-body">{step.desc}</p>
						</div>
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="bg-white py-24">
	<div class="mx-auto max-w-4xl px-4 lg:px-8">
		<ScrollReveal>
			<div class="text-center">
				<h2 class="font-heading text-[clamp(1.5rem,2.5vw,2rem)] font-bold text-dark">Registration Tutorial</h2>
				<p class="mt-3 text-body">Watch this step-by-step guide on how to become a PICPA member</p>
			</div>
		</ScrollReveal>

		<ScrollReveal delay={100}>
			<div class="relative mt-10 overflow-hidden rounded-2xl shadow-xl">
				<video controls class="w-full" poster="/images/logos/emblem.png">
					<source src="https://picpa.com.ph/wp-content/uploads/2023/02/HOW-TO-BECOME-A-MEMBER.mp4" type="video/mp4" />
				</video>
			</div>
		</ScrollReveal>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-4xl px-4 lg:px-8">
		<div class="grid grid-cols-1 gap-8 md:grid-cols-2">
			<ScrollReveal stagger={0}>
				<div class="group relative overflow-hidden rounded-2xl bg-linear-to-br from-primary to-primary-dark p-10 text-center text-white transition-shadow duration-300 hover:shadow-[0_0_40px_rgba(24,179,85,0.3)]">
					<div class="pointer-events-none absolute -top-8 -right-8 h-32 w-32 rounded-full bg-white/10"></div>
					<div class="relative">
						<div class="mx-auto flex h-14 w-14 items-center justify-center rounded-2xl bg-white/20">
							<svg class="h-7 w-7 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
								<path stroke-linecap="round" stroke-linejoin="round" d="M19 7.5v3m0 0v3m0-3h3m-3 0h-3m-2.25-4.125a3.375 3.375 0 11-6.75 0 3.375 3.375 0 016.75 0zM4 19.235v-.11a6.375 6.375 0 0112.75 0v.109A12.318 12.318 0 0110.374 21c-2.331 0-4.512-.645-6.374-1.766z" />
							</svg>
						</div>
						<h3 class="mt-5 font-heading text-xl font-bold">New Member Registration</h3>
						<p class="mt-2 text-sm text-white/80">Register as a new PICPA member through the MELS portal.</p>
						<a
							href="https://picpasystem.com.ph"
							target="_blank"
							rel="noopener noreferrer"
							class="mt-6 inline-flex items-center gap-2 rounded-xl bg-white px-7 py-3 font-medium text-primary transition-all hover:shadow-lg"
						>
							Register Now
							<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
								<path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" />
							</svg>
						</a>
					</div>
				</div>
			</ScrollReveal>

			<ScrollReveal stagger={1}>
				<div class="group relative overflow-hidden rounded-2xl border border-primary/20 bg-white p-10 text-center transition-shadow duration-300 hover:shadow-[0_0_40px_rgba(24,179,85,0.15)]">
					<div class="pointer-events-none absolute -top-8 -right-8 h-32 w-32 rounded-full bg-primary/5"></div>
					<div class="relative">
						<div class="mx-auto flex h-14 w-14 items-center justify-center rounded-2xl bg-primary/10">
							<svg class="h-7 w-7 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
								<path stroke-linecap="round" stroke-linejoin="round" d="M15.75 9V5.25A2.25 2.25 0 0013.5 3h-6a2.25 2.25 0 00-2.25 2.25v13.5A2.25 2.25 0 007.5 21h6a2.25 2.25 0 002.25-2.25V15m3 0l3-3m0 0l-3-3m3 3H9" />
							</svg>
						</div>
						<h3 class="mt-5 font-heading text-xl font-bold text-dark">Existing Member Login</h3>
						<p class="mt-2 text-sm text-body">Access your member account and services.</p>
						<a
							href="https://picpasystem.com.ph/portal/login.html"
							target="_blank"
							rel="noopener noreferrer"
							class="mt-6 inline-flex items-center gap-2 rounded-xl bg-primary px-7 py-3 font-medium text-white transition-all hover:bg-primary-dark hover:shadow-[0_0_20px_rgba(24,179,85,0.3)]"
						>
							Login to MELS
							<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
								<path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" />
							</svg>
						</a>
					</div>
				</div>
			</ScrollReveal>
		</div>
	</div>
</section>

<section class="bg-white py-24">
	<div class="mx-auto max-w-3xl px-4 lg:px-8">
		<ScrollReveal>
			<h2 class="font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-dark">Frequently Asked Questions</h2>
			<p class="mt-3 text-body">Find answers to common questions about PICPA membership.</p>
		</ScrollReveal>

		<div class="mt-12 space-y-4">
			{#each faqs as faq, i (faq.question)}
				<ScrollReveal stagger={i}>
					<div class="overflow-hidden rounded-xl border-l-2 border-primary bg-light transition-colors">
						<button
							class="flex w-full cursor-pointer items-center justify-between px-6 py-5 text-left font-heading font-medium text-dark transition-colors hover:text-primary"
							onclick={() => toggleFaq(i)}
						>
							<span>{faq.question}</span>
							<svg
								class="h-5 w-5 shrink-0 text-primary transition-transform duration-300"
								style="transform: rotate({openFaq === i ? '90deg' : '0deg'});"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor"
								stroke-width="2"
							>
								<path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" />
							</svg>
						</button>
						{#if openFaq === i}
							<div class="px-6 pb-5">
								<p class="leading-relaxed text-body">{faq.answer}</p>
							</div>
						{/if}
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>
