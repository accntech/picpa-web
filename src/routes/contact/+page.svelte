<script lang="ts">
	import PageHero from '$lib/components/PageHero.svelte';
</script>

<PageHero title="Contact Us" breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'Contact' }]} />

<section class="bg-white py-20">
	<div class="mx-auto grid max-w-7xl grid-cols-1 gap-12 px-4 lg:grid-cols-5">
		<div class="lg:col-span-3">
			<h2 class="font-heading text-2xl font-bold text-dark">Get in Touch</h2>
			<p class="mt-2 text-body">
				Have a question or concern? Send us a message and we'll get back to you.
			</p>

			<form class="mt-8 space-y-6">
				<div class="grid grid-cols-1 gap-6 md:grid-cols-2">
					<div>
						<label for="name" class="mb-2 block text-sm font-medium text-dark">Full Name</label>
						<input
							type="text"
							id="name"
							name="name"
							class="w-full rounded-lg border border-gray-200 px-4 py-3 text-dark outline-none transition focus:border-primary focus:ring-1 focus:ring-primary"
						/>
					</div>
					<div>
						<label for="email" class="mb-2 block text-sm font-medium text-dark">Email Address</label>
						<input
							type="email"
							id="email"
							name="email"
							class="w-full rounded-lg border border-gray-200 px-4 py-3 text-dark outline-none transition focus:border-primary focus:ring-1 focus:ring-primary"
						/>
					</div>
				</div>

				<div>
					<label for="subject" class="mb-2 block text-sm font-medium text-dark">Subject</label>
					<input
						type="text"
						id="subject"
						name="subject"
						class="w-full rounded-lg border border-gray-200 px-4 py-3 text-dark outline-none transition focus:border-primary focus:ring-1 focus:ring-primary"
					/>
				</div>

				<div>
					<label for="message" class="mb-2 block text-sm font-medium text-dark">Message</label>
					<textarea
						id="message"
						name="message"
						class="h-40 w-full resize-none rounded-lg border border-gray-200 px-4 py-3 text-dark outline-none transition focus:border-primary focus:ring-1 focus:ring-primary"
					></textarea>
				</div>

				<button
					type="submit"
					class="cursor-pointer rounded-lg bg-primary px-8 py-3 font-medium text-white transition hover:bg-primary-dark"
				>
					Send Message
				</button>
			</form>
		</div>

		<div class="space-y-6 lg:col-span-2">
			<div class="rounded-xl bg-light p-6">
				<div class="flex h-10 w-10 items-center justify-center rounded-lg bg-primary/10">
					<svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
						<path stroke-linecap="round" stroke-linejoin="round" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
						<path stroke-linecap="round" stroke-linejoin="round" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
					</svg>
				</div>
				<h3 class="mt-3 font-heading font-bold text-dark">Office Address</h3>
				<p class="mt-1 text-sm text-body">Shaw Boulevard, Mandaluyong City, 1550 Metro Manila, NCR, Philippines</p>
			</div>

			<div class="rounded-xl bg-light p-6">
				<div class="flex h-10 w-10 items-center justify-center rounded-lg bg-primary/10">
					<svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
						<path stroke-linecap="round" stroke-linejoin="round" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
					</svg>
				</div>
				<h3 class="mt-3 font-heading font-bold text-dark">Phone</h3>
				<p class="mt-1 text-sm text-body">(+632) 8723-0691 to 93</p>
			</div>

			<div class="rounded-xl bg-light p-6">
				<div class="flex h-10 w-10 items-center justify-center rounded-lg bg-primary/10">
					<svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
						<path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
					</svg>
				</div>
				<h3 class="mt-3 font-heading font-bold text-dark">Email</h3>
				<p class="mt-1 text-sm text-body">membership@picpa.com.ph</p>
			</div>

			<div class="rounded-xl bg-light p-6">
				<div class="flex h-10 w-10 items-center justify-center rounded-lg bg-primary/10">
					<svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
						<path stroke-linecap="round" stroke-linejoin="round" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
					</svg>
				</div>
				<h3 class="mt-3 font-heading font-bold text-dark">Office Hours</h3>
				<p class="mt-1 text-sm text-body">Monday - Friday, 8:00 AM - 5:00 PM</p>
			</div>
		</div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="text-center font-heading text-2xl font-bold text-dark">Department Contacts</h2>

		<div class="mt-8 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-4">
			<div class="rounded-xl bg-white p-6 text-center">
				<h3 class="font-heading font-bold text-dark">IT Division</h3>
				<p class="mt-2 break-all text-sm text-primary">techsolutions@picpa.com.ph</p>
			</div>

			<div class="rounded-xl bg-white p-6 text-center">
				<h3 class="font-heading font-bold text-dark">Membership</h3>
				<p class="mt-2 break-all text-sm text-primary">membership@picpa.com.ph</p>
				<p class="mt-3 text-sm text-body">Gener C. Lubi</p>
				<p class="text-xs text-body/70">Viber: (+63) 9175805870</p>
			</div>

			<div class="rounded-xl bg-white p-6 text-center">
				<h3 class="font-heading font-bold text-dark">Administration</h3>
				<p class="mt-2 break-all text-sm text-primary">admin_mgr@picpa.com.ph</p>
				<p class="mt-3 text-sm text-body">Joan C. Quieta</p>
			</div>

			<div class="rounded-xl bg-white p-6 text-center">
				<h3 class="font-heading font-bold text-dark">Training Division</h3>
				<p class="mt-2 break-all text-sm text-primary">training@picpa.com.ph</p>
				<p class="mt-3 text-sm text-body">Salvacion G. Degillo</p>
				<p class="text-xs text-body/70">Phone: (+63) 9199114086</p>
			</div>
		</div>
	</div>
</section>

<section class="bg-white py-16">
	<div class="mx-auto grid max-w-7xl grid-cols-1 gap-8 px-4 lg:grid-cols-2">
		<div class="flex h-64 flex-col items-center justify-center rounded-xl bg-light">
			<svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-body/50" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
				<path stroke-linecap="round" stroke-linejoin="round" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
				<path stroke-linecap="round" stroke-linejoin="round" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
			</svg>
			<p class="mt-3 text-sm text-body">Shaw Boulevard, Mandaluyong City</p>
			<a
				href="https://maps.google.com/?q=PICPA+Shaw+Boulevard+Mandaluyong+City"
				target="_blank"
				rel="noopener noreferrer"
				class="mt-2 text-sm font-medium text-primary transition hover:text-primary-dark"
			>
				View on Google Maps &rarr;
			</a>
		</div>

		<div>
			<h2 class="font-heading text-xl font-bold text-dark">Connect With Us</h2>

			<div class="mt-4 space-y-3">
				<a
					href="https://www.facebook.com/PICPAPhilippines"
					target="_blank"
					rel="noopener noreferrer"
					class="flex items-center gap-3 text-body transition hover:text-primary"
				>
					<svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 24 24" fill="currentColor">
						<path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z" />
					</svg>
					PICPA Philippines
				</a>

				<a
					href="https://www.facebook.com/picpa.nat"
					target="_blank"
					rel="noopener noreferrer"
					class="flex items-center gap-3 text-body transition hover:text-primary"
				>
					<svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 24 24" fill="currentColor">
						<path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z" />
					</svg>
					PICPA National Office
				</a>
			</div>
		</div>
	</div>
</section>
