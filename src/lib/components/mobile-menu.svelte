<script lang="ts">
	let { open, onclose }: { open: boolean; onclose: () => void } = $props();

	let expandedSection = $state<string | null>(null);

	const dropdowns = [
		{
			key: 'about',
			label: 'About',
			children: [
				{ label: 'About PICPA', href: '/about' },
				{ label: 'Vision & Mission', href: '/about/vision-mission' },
				{ label: 'Officers', href: '/about/officers' },
				{ label: "President's Corner", href: '/about/presidents-corner' }
			]
		},
		{
			key: 'community',
			label: 'Community',
			children: [
				{ label: 'Members', href: '/members' },
				{ label: 'Chapters', href: '/chapters' },
				{ label: 'Journal', href: '/journal' }
			]
		}
	];

	const mainLinks = [
		{ label: 'Events', href: '/events' },
		{ label: 'Careers', href: '/careers' },
		{ label: 'Foundation', href: '/foundation' },
		{ label: 'Contact', href: '/contact' }
	];

	function handleBackdropClick() {
		onclose();
	}

	function handleKeydown(e: KeyboardEvent) {
		if (e.key === 'Escape') onclose();
	}

	function toggleSection(key: string) {
		expandedSection = expandedSection === key ? null : key;
	}
</script>

{#if open}
	<!-- svelte-ignore a11y_no_static_element_interactions -->
	<div class="fixed inset-0 z-50" onkeydown={handleKeydown}>
		<div
			class="absolute inset-0 bg-black/40 backdrop-blur-sm"
			onclick={handleBackdropClick}
			role="presentation"
		></div>

		<div
			class="absolute right-0 top-0 h-full w-80 max-w-full overflow-y-auto bg-white shadow-2xl transition-transform"
		>
			<div class="flex items-center justify-between border-b border-gray-100 px-5 py-4">
				<a href="/" onclick={onclose}>
					<img src="/images/logos/dark-logo.png" alt="PICPA Logo" class="h-9" />
				</a>
				<button onclick={onclose} class="cursor-pointer text-dark" aria-label="Close menu">
					<svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M6 18L18 6M6 6l12 12"
						/>
					</svg>
				</button>
			</div>

			<nav class="px-5 py-4">
				<ul class="space-y-1">
					{#each dropdowns as dropdown, i (dropdown.key)}
						<li>
							<button
								class="flex w-full cursor-pointer items-center justify-between rounded-lg px-3 py-2.5 text-sm font-medium text-dark transition-colors hover:bg-light hover:text-primary"
								onclick={() => toggleSection(dropdown.key)}
							>
								{dropdown.label}
								<span class="inline-block text-base transition-transform {expandedSection === dropdown.key ? 'rotate-90' : ''}">&raquo;</span>
							</button>
							{#if expandedSection === dropdown.key}
								<ul class="ml-3 space-y-1 border-l-2 border-primary/20 pl-3">
									{#each dropdown.children as child (child.href)}
										<li>
											<a
												href={child.href}
												onclick={onclose}
												class="block rounded-lg px-3 py-2 text-sm text-body transition-colors hover:text-primary"
											>
												{child.label}
											</a>
										</li>
									{/each}
								</ul>
							{/if}
						</li>
						{#if i === 0}
							{#each mainLinks.slice(0, 3) as link (link.href)}
								<li>
									<a
										href={link.href}
										onclick={onclose}
										class="block rounded-lg px-3 py-2.5 text-sm font-medium text-dark transition-colors hover:bg-light hover:text-primary"
									>
										{link.label}
									</a>
								</li>
							{/each}
						{/if}
					{/each}
					{#each mainLinks.slice(3) as link (link.href)}
						<li>
							<a
								href={link.href}
								onclick={onclose}
								class="block rounded-lg px-3 py-2.5 text-sm font-medium text-dark transition-colors hover:bg-light hover:text-primary"
							>
								{link.label}
							</a>
						</li>
					{/each}
				</ul>
			</nav>

			<div class="px-5 pb-6">
				<a
					href="https://picpasystem.com.ph/portal/login.html" target="_blank" rel="noopener noreferrer"
					onclick={onclose}
					class="block rounded-lg bg-primary px-5 py-3 text-center text-sm font-medium text-white transition-colors hover:bg-primary-dark"
				>
					My MELS Account
				</a>
			</div>
		</div>
	</div>
{/if}
