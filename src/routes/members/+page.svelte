<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';

	const benefits = [
		{
			icon: '📚',
			title: 'Professional Development',
			desc: 'Access to CPD seminars, workshops, conferences, and the PICPA Academy for continuous learning.'
		},
		{
			icon: '🤝',
			title: 'Networking',
			desc: 'Connect with over 26,000 active members across 84 local and 17 international chapters.'
		},
		{
			icon: '📝',
			title: 'CPD Credits',
			desc: 'Earn continuing professional development credits required for CPA license renewal.'
		},
		{
			icon: '💼',
			title: 'Career Support',
			desc: 'Free job posting service, career resources, and access to the PICPA careers portal.'
		},
		{
			icon: '📢',
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
</script>

<PageHero title="Member Services" breadcrumbs={[{label: 'Home', href: '/'}, {label: 'Members'}]} />

<!-- Benefits -->
<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="text-center font-heading text-3xl font-bold text-dark">Why Join PICPA?</h2>

		<div class="mt-12 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each benefits as benefit (benefit.title)}
				<div class="rounded-xl bg-light p-6">
					<span class="text-3xl">{benefit.icon}</span>
					<h3 class="mt-3 font-heading text-lg font-bold text-dark">{benefit.title}</h3>
					<p class="mt-2 text-sm text-body">{benefit.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- Registration Steps -->
<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="text-center font-heading text-3xl font-bold text-dark">How to Register</h2>
		<p class="mt-3 text-center text-body">Follow these 5 simple steps to become a PICPA member</p>

		<div class="mt-12 flex flex-col gap-4 lg:flex-row">
			{#each steps as step, i (step.number)}
				<div class="relative flex-1 rounded-xl bg-white p-6 text-center shadow-sm">
					<div class="mx-auto flex h-10 w-10 items-center justify-center rounded-full bg-primary text-lg font-bold text-white">
						{step.number}
					</div>
					<h3 class="mt-4 font-heading text-lg font-bold text-dark">{step.title}</h3>
					<p class="mt-2 text-sm text-body">{step.desc}</p>
				</div>
				{#if i < steps.length - 1}
					<div class="hidden items-center lg:flex">
						<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
							<path stroke-linecap="round" stroke-linejoin="round" d="M9 5l7 7-7 7" />
						</svg>
					</div>
				{/if}
			{/each}
		</div>
	</div>
</section>

<!-- Video Tutorial -->
<section class="bg-white py-20">
	<div class="mx-auto max-w-4xl px-4 text-center">
		<h2 class="font-heading text-2xl font-bold text-dark">Registration Tutorial</h2>
		<p class="mt-3 text-body">Watch this step-by-step guide on how to become a PICPA member</p>

		<div class="mt-8 overflow-hidden rounded-2xl shadow-lg">
			<video controls class="w-full" poster="/images/logos/emblem.png">
				<source src="https://picpa.com.ph/wp-content/uploads/2023/02/HOW-TO-BECOME-A-MEMBER.mp4" type="video/mp4" />
			</video>
		</div>
	</div>
</section>

<!-- MELS Links -->
<section class="bg-light py-16">
	<div class="mx-auto max-w-4xl px-4">
		<div class="grid grid-cols-1 gap-6 md:grid-cols-2">
			<div class="rounded-xl bg-primary p-8 text-center text-white">
				<h3 class="font-heading text-xl font-bold">New Member Registration</h3>
				<p class="mt-2 text-sm text-white/80">Register as a new PICPA member through the MELS portal.</p>
				<a
					href="https://picpasystem.com.ph"
					target="_blank"
					rel="noopener noreferrer"
					class="mt-4 inline-block rounded-lg bg-white px-6 py-2.5 font-medium text-primary"
				>
					Register Now
				</a>
			</div>

			<div class="rounded-xl border-2 border-primary bg-white p-8 text-center">
				<h3 class="font-heading text-xl font-bold text-dark">Existing Member Login</h3>
				<p class="mt-2 text-sm text-body">Access your member account and services.</p>
				<a
					href="https://picpasystem.com.ph/portal/login.html"
					target="_blank"
					rel="noopener noreferrer"
					class="mt-4 inline-block rounded-lg bg-primary px-6 py-2.5 font-medium text-white"
				>
					Login to MELS
				</a>
			</div>
		</div>
	</div>
</section>

<!-- FAQ -->
<section class="bg-white py-20">
	<div class="mx-auto max-w-4xl px-4">
		<h2 class="text-center font-heading text-2xl font-bold text-dark">Frequently Asked Questions</h2>

		<div class="mt-8 space-y-3">
			{#each faqs as faq (faq.question)}
				<details class="group overflow-hidden rounded-xl bg-light">
					<summary class="flex cursor-pointer items-center justify-between px-6 py-4 font-heading font-medium text-dark transition hover:text-primary">
						{faq.question}
						<svg
							class="h-5 w-5 shrink-0 transition-transform group-open:rotate-45"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							stroke-width="2"
						>
							<path stroke-linecap="round" stroke-linejoin="round" d="M12 4v16m8-8H4" />
						</svg>
					</summary>
					<p class="px-6 pb-4 text-body">{faq.answer}</p>
				</details>
			{/each}
		</div>
	</div>
</section>
