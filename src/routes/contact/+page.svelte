<script lang="ts">
	import PageHero from '$lib/components/page-hero.svelte';
	import ScrollReveal from '$lib/components/scroll-reveal.svelte';

	const departments = [
		{
			name: 'IT Division',
			email: 'techsolutions@picpa.com.ph'
		},
		{
			name: 'Membership',
			email: 'membership@picpa.com.ph',
			contact: 'Gener C. Lubi',
			phone: 'Viber: (+63) 9175805870'
		},
		{
			name: 'Administration',
			email: 'admin_mgr@picpa.com.ph',
			contact: 'Joan C. Quieta'
		},
		{
			name: 'Training Division',
			email: 'training@picpa.com.ph',
			contact: 'Salvacion G. Degillo',
			phone: 'Phone: (+63) 9199114086'
		}
	];
</script>

<PageHero title="Contact Us" breadcrumbs={[{label: 'Home', href: '/'}, {label: 'Contact'}]} />

<section class="bg-white py-24">
	<div class="mx-auto grid max-w-7xl grid-cols-1 gap-16 px-4 lg:grid-cols-5 lg:px-8">
		<div class="lg:col-span-3">
			<ScrollReveal>
				<h2 class="font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-dark">Get in Touch</h2>
				<p class="mt-3 text-body">
					Have a question or concern? Send us a message and we'll get back to you.
				</p>
			</ScrollReveal>

			<ScrollReveal delay={100}>
				<form class="mt-10 space-y-6">
					<div class="grid grid-cols-1 gap-6 md:grid-cols-2">
						<div class="relative">
							<input
								type="text"
								id="name"
								name="name"
								placeholder=" "
								class="peer w-full rounded-xl border border-gray-200 bg-transparent px-4 pt-6 pb-2 text-dark outline-none transition-all focus:border-primary focus:ring-1 focus:ring-primary"
							/>
							<label
								for="name"
								class="pointer-events-none absolute top-4 left-4 text-sm text-body transition-all peer-focus:top-1.5 peer-focus:text-xs peer-focus:text-primary peer-[:not(:placeholder-shown)]:top-1.5 peer-[:not(:placeholder-shown)]:text-xs"
							>
								Full Name
							</label>
						</div>
						<div class="relative">
							<input
								type="email"
								id="email"
								name="email"
								placeholder=" "
								class="peer w-full rounded-xl border border-gray-200 bg-transparent px-4 pt-6 pb-2 text-dark outline-none transition-all focus:border-primary focus:ring-1 focus:ring-primary"
							/>
							<label
								for="email"
								class="pointer-events-none absolute top-4 left-4 text-sm text-body transition-all peer-focus:top-1.5 peer-focus:text-xs peer-focus:text-primary peer-[:not(:placeholder-shown)]:top-1.5 peer-[:not(:placeholder-shown)]:text-xs"
							>
								Email Address
							</label>
						</div>
					</div>

					<div class="relative">
						<input
							type="text"
							id="subject"
							name="subject"
							placeholder=" "
							class="peer w-full rounded-xl border border-gray-200 bg-transparent px-4 pt-6 pb-2 text-dark outline-none transition-all focus:border-primary focus:ring-1 focus:ring-primary"
						/>
						<label
							for="subject"
							class="pointer-events-none absolute top-4 left-4 text-sm text-body transition-all peer-focus:top-1.5 peer-focus:text-xs peer-focus:text-primary peer-[:not(:placeholder-shown)]:top-1.5 peer-[:not(:placeholder-shown)]:text-xs"
						>
							Subject
						</label>
					</div>

					<div class="relative">
						<textarea
							id="message"
							name="message"
							placeholder=" "
							class="peer h-40 w-full resize-none rounded-xl border border-gray-200 bg-transparent px-4 pt-6 pb-2 text-dark outline-none transition-all focus:border-primary focus:ring-1 focus:ring-primary"
						></textarea>
						<label
							for="message"
							class="pointer-events-none absolute top-4 left-4 text-sm text-body transition-all peer-focus:top-1.5 peer-focus:text-xs peer-focus:text-primary peer-[:not(:placeholder-shown)]:top-1.5 peer-[:not(:placeholder-shown)]:text-xs"
						>
							Message
						</label>
					</div>

					<button
						type="submit"
						class="inline-flex cursor-pointer items-center gap-2 rounded-xl bg-primary px-8 py-3.5 font-medium text-white transition-all hover:bg-primary-dark hover:shadow-[0_0_20px_rgba(24,179,85,0.3)]"
					>
						Send Message
						<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
							<path stroke-linecap="round" stroke-linejoin="round" d="M6 12L3.269 3.126A59.768 59.768 0 0121.485 12 59.77 59.77 0 013.27 20.876L5.999 12zm0 0h7.5" />
						</svg>
					</button>
				</form>
			</ScrollReveal>
		</div>

		<div class="space-y-6 lg:col-span-2">
			<ScrollReveal stagger={0}>
				<div class="rounded-2xl bg-light p-6 transition-all duration-300 hover:shadow-md">
					<div class="flex h-11 w-11 items-center justify-center rounded-xl bg-primary/10">
						<svg class="h-5 w-5 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
							<path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
							<path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
						</svg>
					</div>
					<h3 class="mt-4 font-heading font-bold text-dark">Office Address</h3>
					<p class="mt-1 text-sm leading-relaxed text-body">Shaw Boulevard, Mandaluyong City, 1550 Metro Manila, NCR, Philippines</p>
				</div>
			</ScrollReveal>

			<ScrollReveal stagger={1}>
				<div class="rounded-2xl bg-light p-6 transition-all duration-300 hover:shadow-md">
					<div class="flex h-11 w-11 items-center justify-center rounded-xl bg-primary/10">
						<svg class="h-5 w-5 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
							<path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z" />
						</svg>
					</div>
					<h3 class="mt-4 font-heading font-bold text-dark">Phone</h3>
					<p class="mt-1 text-sm text-body">(+632) 8723-0691 to 93</p>
				</div>
			</ScrollReveal>

			<ScrollReveal stagger={2}>
				<div class="rounded-2xl bg-light p-6 transition-all duration-300 hover:shadow-md">
					<div class="flex h-11 w-11 items-center justify-center rounded-xl bg-primary/10">
						<svg class="h-5 w-5 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
							<path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75" />
						</svg>
					</div>
					<h3 class="mt-4 font-heading font-bold text-dark">Email</h3>
					<p class="mt-1 text-sm text-body">membership@picpa.com.ph</p>
				</div>
			</ScrollReveal>

			<ScrollReveal stagger={3}>
				<div class="rounded-2xl bg-light p-6 transition-all duration-300 hover:shadow-md">
					<div class="flex h-11 w-11 items-center justify-center rounded-xl bg-primary/10">
						<svg class="h-5 w-5 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
							<path stroke-linecap="round" stroke-linejoin="round" d="M12 6v6h4.5m4.5 0a9 9 0 11-18 0 9 9 0 0118 0z" />
						</svg>
					</div>
					<h3 class="mt-4 font-heading font-bold text-dark">Office Hours</h3>
					<p class="mt-1 text-sm text-body">Monday - Friday, 8:00 AM - 5:00 PM</p>
				</div>
			</ScrollReveal>
		</div>
	</div>
</section>

<section class="relative overflow-hidden bg-navy py-24">
	<div class="gradient-mesh-bg absolute inset-0"></div>
	<svg class="pointer-events-none absolute top-12 right-16 h-48 w-48 text-white/3" style="animation: float 6s ease-in-out infinite;" viewBox="0 0 87 85" fill="currentColor">
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto max-w-7xl px-4 lg:px-8">
		<ScrollReveal>
			<h2 class="font-heading text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-white">Department Contacts</h2>
			<p class="mt-3 text-slate">Reach out directly to the department that can best assist you.</p>
		</ScrollReveal>

		<div class="mt-14 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-4">
			{#each departments as dept, i (dept.name)}
				<ScrollReveal stagger={i}>
					<div class="glass rounded-2xl p-7 text-center transition-all duration-300 hover:-translate-y-0.5 hover:shadow-[0_0_30px_rgba(24,179,85,0.1)]">
						<div class="mx-auto flex h-12 w-12 items-center justify-center rounded-xl bg-primary/10">
							<svg class="h-6 w-6 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
								<path stroke-linecap="round" stroke-linejoin="round" d="M2.25 21h19.5m-18-18v18m10.5-18v18m6-13.5V21M6.75 6.75h.75m-.75 3h.75m-.75 3h.75m3-6h.75m-.75 3h.75m-.75 3h.75M6.75 21v-3.375c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21M3 3h12m-.75 4.5H21m-3.75 3h.008v.008h-.008v-.008zm0 3h.008v.008h-.008v-.008zm0 3h.008v.008h-.008v-.008z" />
							</svg>
						</div>
						<h3 class="mt-4 font-heading font-bold text-white">{dept.name}</h3>
						<a href="mailto:{dept.email}" class="mt-2 block break-all text-sm text-primary transition-colors hover:text-primary/80">{dept.email}</a>
						{#if dept.contact}
							<p class="mt-3 text-sm text-white/70">{dept.contact}</p>
						{/if}
						{#if dept.phone}
							<p class="text-xs text-white/50">{dept.phone}</p>
						{/if}
					</div>
				</ScrollReveal>
			{/each}
		</div>
	</div>
</section>

<section class="bg-white py-20">
	<div class="mx-auto grid max-w-7xl grid-cols-1 gap-12 px-4 lg:grid-cols-2 lg:px-8">
		<ScrollReveal>
			<div class="overflow-hidden rounded-2xl shadow-xl">
				<iframe
					src="https://www.google.com/maps/embed?pb=!4v1772549279924!6m8!1m7!1s_11TiCeydMYLFMLvVA_bqQ!2m2!1d14.58411813307402!2d121.0503369038619!3f9.518523622264699!4f8.775839773605469!5f0.7820865974627469"
					width="100%"
					height="360"
					style="border:0;"
					allowfullscreen
					loading="lazy"
					referrerpolicy="no-referrer-when-downgrade"
					title="PICPA Office Location"
				></iframe>
			</div>
		</ScrollReveal>

		<ScrollReveal delay={100}>
			<div>
				<h2 class="font-heading text-[clamp(1.5rem,2.5vw,2rem)] font-bold text-dark">Connect With Us</h2>
				<p class="mt-3 text-body">Follow PICPA on social media for the latest updates, events, and announcements.</p>

				<div class="mt-8 space-y-4">
					<a
						href="https://www.facebook.com/PICPAPhilippines"
						target="_blank"
						rel="noopener noreferrer"
						class="group flex items-center gap-4 rounded-xl border border-gray-100 bg-white p-4 transition-all duration-300 hover:border-primary/20 hover:shadow-md"
					>
						<div class="flex h-11 w-11 items-center justify-center rounded-xl bg-primary/10 transition-colors group-hover:bg-primary/20">
							<svg class="h-5 w-5 text-primary" viewBox="0 0 24 24" fill="currentColor">
								<path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z" />
							</svg>
						</div>
						<div class="flex-1">
							<span class="font-heading font-medium text-dark">PICPA Philippines</span>
							<p class="text-xs text-body">Official Facebook Page</p>
						</div>
						<span class="translate-x-0 text-primary opacity-0 transition-all duration-300 group-hover:translate-x-1 group-hover:opacity-100">&raquo;</span>
					</a>

					<a
						href="https://www.facebook.com/picpa.nat"
						target="_blank"
						rel="noopener noreferrer"
						class="group flex items-center gap-4 rounded-xl border border-gray-100 bg-white p-4 transition-all duration-300 hover:border-primary/20 hover:shadow-md"
					>
						<div class="flex h-11 w-11 items-center justify-center rounded-xl bg-primary/10 transition-colors group-hover:bg-primary/20">
							<svg class="h-5 w-5 text-primary" viewBox="0 0 24 24" fill="currentColor">
								<path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z" />
							</svg>
						</div>
						<div class="flex-1">
							<span class="font-heading font-medium text-dark">PICPA National Office</span>
							<p class="text-xs text-body">National Office Facebook Page</p>
						</div>
						<span class="translate-x-0 text-primary opacity-0 transition-all duration-300 group-hover:translate-x-1 group-hover:opacity-100">&raquo;</span>
					</a>
				</div>
			</div>
		</ScrollReveal>
	</div>
</section>
