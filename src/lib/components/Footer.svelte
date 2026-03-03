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

<footer class="bg-primary-deep">
	<div class="mx-auto max-w-7xl px-4 py-16 lg:px-8">
		<div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-4">
			<div>
				<img src="/images/logos/light-logo.png" alt="PICPA Logo" class="mb-4 h-10" />
				<p class="text-sm leading-relaxed text-white/70">
					The national professional organization for CPAs in the Philippines, founded in 1929.
				</p>
			</div>

			<div>
				<h3 class="mb-4 text-sm font-semibold tracking-wider text-white uppercase">
					Quick Links
				</h3>
				<ul class="space-y-2.5">
					{#each quickLinks as link (link.href)}
						<li>
							<a
								href={link.href}
								class="text-sm text-white/70 transition-colors hover:text-primary"
							>
								{link.label}
							</a>
						</li>
					{/each}
				</ul>
			</div>

			<div>
				<h3 class="mb-4 text-sm font-semibold tracking-wider text-white uppercase">
					Contact
				</h3>
				<div class="space-y-2.5 text-sm text-white/70">
					<p>Shaw Boulevard, Mandaluyong City, 1550 Metro Manila</p>
					<p>Phone: (+632) 8723-0691 to 93</p>
					<p>
						Email:
						<a
							href="mailto:membership@picpa.com.ph"
							class="transition-colors hover:text-primary"
						>
							membership@picpa.com.ph
						</a>
					</p>
				</div>
			</div>

			<div>
				<h3 class="mb-4 text-sm font-semibold tracking-wider text-white uppercase">
					Connect
				</h3>
				<div class="space-y-4">
					<a
						href="https://www.facebook.com/PICPAPhilippines"
						target="_blank"
						rel="noopener noreferrer"
						class="inline-flex items-center gap-2 text-sm text-white/70 transition-colors hover:text-primary"
					>
						<svg class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
							<path
								d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"
							/>
						</svg>
						Facebook
					</a>
					<div>
						<a
							href="https://picpasystem.com.ph/portal/login.html" target="_blank" rel="noopener noreferrer"
							class="inline-block rounded-lg bg-primary px-5 py-2.5 text-sm font-medium text-white transition-colors hover:bg-primary-dark"
						>
							My MELS Account
						</a>
					</div>
				</div>
			</div>
		</div>
	</div>

	<div class="border-t border-white/20">
		<div class="mx-auto max-w-7xl px-4 py-6 lg:px-8">
			<p class="text-center text-sm text-white/50">
				&copy; 2026 PICPA - Philippine Institute of Certified Public Accountants
			</p>
		</div>
	</div>
</footer>
