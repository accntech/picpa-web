<script lang="ts">
	const quickLinks = [
		{ label: 'About PICPA', href: '/about' },
		{ label: 'Vision & Mission', href: '/about/vision-mission' },
		{ label: 'Events', href: '/events' },
		{ label: 'Careers', href: '/careers' },
		{ label: 'Foundation', href: '/foundation' },
		{ label: 'Chapters', href: '/chapters' }
	];
</script>

<footer class="relative bg-navy overflow-hidden">
	<div class="-top-20 -right-20 absolute opacity-30 w-96 h-96 pointer-events-none gradient-mesh-bg"></div>

	<svg
		class="-right-10 -bottom-10 absolute opacity-[0.025] w-80 h-80 text-white pointer-events-none"
		viewBox="0 0 87 85"
		fill="currentColor"
	>
		<polygon points="33,84 14,57 33,28 19,28 0,57 19,84" />
		<polygon points="51,84 32,57 51,28 37,28 18,57 37,84" />
		<polygon points="36,57 55,29 36,0 50,0 69,29 50,57" />
		<polygon points="54,57 73,29 54,0 68,0 87,29 68,57" />
	</svg>

	<div class="relative mx-auto px-4 lg:px-8 py-16 max-w-7xl">
		<div class="gap-8 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5">
			<div class="lg:col-span-1">
				<img src="/images/logos/light-logo.png" alt="PICPA Logo" class="pb-2 shrink-0" />
				<p class="text-white/40 text-xs leading-relaxed tracking-wide">
					Est. 1929 — The National Organization of CPAs
				</p>
				<p class="mt-3 text-white/70 text-sm leading-relaxed">
					The national professional organization for CPAs in the Philippines.
				</p>
			</div>

			<div>
				<h3 class="mb-4 font-semibold text-white text-sm uppercase tracking-wider">
					Quick Links
				</h3>
				<ul class="space-y-2.5">
					{#each quickLinks as link (link.href)}
						<li>
							<a
								href={link.href}
								class="group inline-flex items-center gap-1 text-white/70 hover:text-primary text-sm transition-colors"
							>
								<span class="opacity-0 group-hover:opacity-100 transition -translate-x-1 group-hover:translate-x-0 duration-200">&raquo;</span>
								<span>{link.label}</span>
							</a>
						</li>
					{/each}
				</ul>
			</div>

			<div>
				<h3 class="mb-4 font-semibold text-white text-sm uppercase tracking-wider">
					Contact
				</h3>
				<div class="space-y-2.5 text-white/70 text-sm">
					<p>Shaw Boulevard, Mandaluyong City, 1550 Metro Manila</p>
					<p>Phone: (+632) 8723-0691 to 93</p>
					<p>
						Email:
						<a
							href="mailto:membership@picpa.com.ph"
							class="hover:text-primary transition-colors"
						>
							membership@picpa.com.ph
						</a>
					</p>
				</div>
			</div>

			<div>
				<h3 class="mb-4 font-semibold text-white text-sm uppercase tracking-wider">
					Connect
				</h3>
				<div class="space-y-4">
					<a
						href="https://www.facebook.com/PICPAPhilippines"
						target="_blank"
						rel="noopener noreferrer"
						class="group inline-flex items-center gap-2 text-white/70 hover:text-primary text-sm transition-colors"
					>
						<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
							<path
								d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"
							/>
						</svg>
						Facebook
					</a>
					<div>
						<a
							href="https://picpasystem.com.ph/portal/login.html"
							target="_blank"
							rel="noopener noreferrer"
							class="inline-block bg-primary hover:bg-primary-dark px-5 py-2.5 rounded-lg font-medium text-white text-sm transition-colors"
						>
							My MELS Account
						</a>
					</div>
				</div>
			</div>

			<div>
				<h3 class="mb-4 font-semibold text-white text-sm uppercase tracking-wider">
					Stay Updated
				</h3>
				<p class="mb-4 text-white/70 text-sm">
					Get the latest PICPA news and events delivered to your inbox.
				</p>
				<form onsubmit={(e) => e.preventDefault()} class="flex flex-col gap-3">
					<input
						type="email"
						placeholder="Your email address"
						class="bg-white/10 backdrop-blur-sm px-4 py-2.5 border border-white/20 focus:border-primary/50 rounded-lg outline-none focus:ring-1 focus:ring-primary/30 text-white text-sm transition placeholder-white/40"
					/>
					<button
						type="button"
						class="bg-primary hover:bg-primary-dark px-4 py-2.5 rounded-lg font-medium text-white text-sm transition-colors"
					>
						Subscribe
					</button>
				</form>
			</div>
		</div>
	</div>

	<div class="border-white/10 border-t">
		<div class="mx-auto px-4 lg:px-8 py-6 max-w-7xl text-center">
			<p class="text-white/50 text-sm">
				&copy; 2026 PICPA - Philippine Institute of Certified Public Accountants
			</p>
			<p class="mt-2 text-white/50 text-xs">
				Powered by
				<a
					href="https://accountech.dev"
					target="_blank"
					rel="noopener noreferrer"
					class="group inline font-bold text-foreground/80 hover:text-foreground transition-colors"
				>
					accoun<span
						class="text-teal-400 group-hover:text-teal-300 transition-colors"
					>tech</span><span class="text-teal-400">.</span>
				</a>
			</p>
		</div>
	</div>
</footer>
