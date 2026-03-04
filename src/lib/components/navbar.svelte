<script lang="ts">
	import MobileMenu from './mobile-menu.svelte';

	let { transparent = false }: { transparent?: boolean } = $props();

	let scrolled = $state(false);
	let mobileOpen = $state(false);
	let activeDropdown = $state<string | null>(null);
	let clickLocked = $state(false);

	$effect(() => {
		function onScroll() {
			scrolled = window.scrollY > 50;
		}
		onScroll();
		window.addEventListener('scroll', onScroll, { passive: true });
		return () => window.removeEventListener('scroll', onScroll);
	});

	$effect(() => {
		document.body.style.overflow = mobileOpen ? 'hidden' : '';
		return () => { document.body.style.overflow = ''; };
	});

	const navLinks = [
		{
			label: 'About',
			href: '/about',
			key: 'about',
			children: [
				{
					label: 'About PICPA',
					desc: 'Who we are and what we stand for',
					href: '/about',
					icon: 'building'
				},
				{
					label: 'Vision & Mission',
					desc: 'Our guiding principles',
					href: '/about/vision-mission',
					icon: 'target'
				},
				{
					label: 'Officers',
					desc: 'National board & leadership',
					href: '/about/officers',
					icon: 'users'
				},
				{
					label: "President's Corner",
					desc: 'Message from the president',
					href: '/about/presidents-corner',
					icon: 'message'
				}
			]
		},
		{ label: 'Events', href: '/events' },
		{ label: 'Careers', href: '/careers' },
		{ label: 'Foundation', href: '/foundation' },
		{
			label: 'Community',
			href: '/members',
			key: 'community',
			children: [
				{
					label: 'Members',
					desc: 'Membership benefits & directory',
					href: '/members',
					icon: 'card'
				},
				{
					label: 'Chapters',
					desc: 'Find your local chapter',
					href: '/chapters',
					icon: 'map'
				},
				{
					label: 'Journal',
					desc: 'The Accountant journal archive',
					href: '/journal',
					icon: 'book'
				}
			]
		},
		{ label: 'Contact', href: '/contact' }
	];

	let isTransparent = $derived(transparent && !scrolled);

	$effect(() => {
		if (!activeDropdown) return;
		const close = () => { activeDropdown = null; clickLocked = false; };
		window.addEventListener('click', close);
		return () => window.removeEventListener('click', close);
	});
</script>

<header
	class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 {isTransparent
		? 'bg-transparent'
		: 'bg-white/80 backdrop-blur-xl shadow-sm'}"
>
	<nav class="flex justify-between items-center mx-auto px-4 lg:px-8 py-3 max-w-7xl">
		<a href="/">
			<img
				src={isTransparent ? '/images/logos/light-logo.png' : '/images/logos/dark-logo.png'}
				alt="PICPA Logo"
				class="h-10 shrink-0"
			/>
		</a>

		<ul class="hidden lg:flex items-center gap-1">
			{#each navLinks as link (link.href)}
				<!-- svelte-ignore a11y_no_static_element_interactions -->
				<li
					class="relative"
					onmouseenter={() => link.children && !clickLocked && (activeDropdown = link.key)}
					onmouseleave={() => link.children && !clickLocked && (activeDropdown = null)}
				>
					{#if link.children}
						{@const isOpen = activeDropdown === link.key}
						<button
							class="relative cursor-pointer px-3 py-2 text-sm font-medium transition-colors after:absolute after:bottom-0 after:left-3 after:right-3 after:h-0.5 after:origin-left after:scale-x-0 after:bg-primary after:transition-transform hover:text-primary hover:after:scale-x-100 {isTransparent
								? 'text-white'
								: 'text-dark'}"
							onclick={(e: MouseEvent) => { e.stopPropagation(); if (isOpen) { activeDropdown = null; clickLocked = false; } else { activeDropdown = link.key; clickLocked = true; } }}
						>
							{link.label}
							<svg
								class="ml-1 inline-block h-3 w-3 transition-transform {isOpen
									? 'rotate-180'
									: ''}"
								fill="none"
								stroke="currentColor"
								viewBox="0 0 24 24"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M19 9l-7 7-7-7"
								/>
							</svg>
						</button>
						{#if isOpen}
							<div
								class="dropdown-panel"
								role="menu"
								tabindex="-1"
								onclick={(e: MouseEvent) => e.stopPropagation()}
								onkeydown={(e: KeyboardEvent) => { if (e.key === 'Escape') activeDropdown = null; }}
							>
								<div class="top-0 right-4 left-4 absolute bg-linear-to-r from-transparent via-primary to-transparent h-px"></div>
								{#each link.children as child, i (child.href)}
									<a
										href={child.href}
										class="dropdown-item"
										style="animation-delay: {i * 40}ms"
									>
										<span class="dropdown-icon">
											{#if child.icon === 'building'}
												<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M3 21h18M5 21V7l8-4v18M19 21V11l-6-4M9 9v.01M9 12v.01M9 15v.01M9 18v.01"/></svg>
											{:else if child.icon === 'target'}
												<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><circle cx="12" cy="12" r="6"/><circle cx="12" cy="12" r="2"/></svg>
											{:else if child.icon === 'users'}
												<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87M16 3.13a4 4 0 0 1 0 7.75"/></svg>
											{:else if child.icon === 'message'}
												<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></svg>
											{:else if child.icon === 'card'}
												<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="5" width="20" height="14" rx="2"/><line x1="2" y1="10" x2="22" y2="10"/></svg>
											{:else if child.icon === 'map'}
												<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
											{:else if child.icon === 'book'}
												<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/><path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/></svg>
											{/if}
										</span>
										<span>
											<span class="dropdown-label">{child.label}</span>
											<span class="dropdown-desc">{child.desc}</span>
										</span>
										<span class="dropdown-chevron">&raquo;</span>
									</a>
								{/each}
							</div>
						{/if}
					{:else}
						<a
							href={link.href}
							class="relative block px-3 py-2 text-sm font-medium transition-colors after:absolute after:bottom-0 after:left-3 after:right-3 after:h-0.5 after:origin-left after:scale-x-0 after:bg-primary after:transition-transform hover:text-primary hover:after:scale-x-100 {isTransparent
								? 'text-white'
								: 'text-dark'}"
						>
							{link.label}
						</a>
					{/if}
				</li>
			{/each}
		</ul>

		<div class="hidden lg:block">
			<a
				href="https://picpasystem.com.ph/portal/login.html" target="_blank" rel="noopener noreferrer"
				class="bg-primary hover:bg-primary-dark hover:shadow-[0_0_20px_rgba(24,179,85,0.3)] px-5 py-2.5 rounded-lg font-medium text-white text-sm text-nowrap transition-all"
			>
				My MELS Account
			</a>
		</div>

		<button
			class="cursor-pointer lg:hidden {isTransparent ? 'text-white' : 'text-dark'}"
			onclick={() => (mobileOpen = true)}
			aria-label="Open menu"
		>
			<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					stroke-width="2"
					d="M4 6h16M4 12h16M4 18h16"
				/>
			</svg>
		</button>
	</nav>
</header>

<MobileMenu open={mobileOpen} onclose={() => (mobileOpen = false)} />

<style>
	.dropdown-panel::before {
		content: '';
		position: absolute;
		top: -12px;
		left: 0;
		right: 0;
		height: 12px;
	}

	.dropdown-panel {
		position: absolute;
		top: calc(100% + 4px);
		left: 50%;
		transform: translateX(-50%);
		min-width: 300px;
		padding: 12px 8px;
		background: rgba(255, 255, 255, 0.92);
		backdrop-filter: blur(20px);
		-webkit-backdrop-filter: blur(20px);
		border: 1px solid rgba(0, 0, 0, 0.06);
		border-radius: 16px;
		box-shadow:
			0 20px 40px -12px rgba(0, 0, 0, 0.12),
			0 0 0 1px rgba(0, 0, 0, 0.03);
		animation: dropdown-in 0.2s cubic-bezier(0.22, 1, 0.36, 1);
	}

	.dropdown-item {
		display: flex;
		align-items: center;
		gap: 12px;
		padding: 10px 12px;
		border-radius: 10px;
		text-decoration: none;
		transition: all 0.15s ease;
		animation: item-in 0.25s cubic-bezier(0.22, 1, 0.36, 1) both;
	}

	.dropdown-item:hover {
		background: rgba(24, 179, 85, 0.06);
	}

	.dropdown-item:hover .dropdown-icon {
		color: var(--color-primary);
		background: rgba(24, 179, 85, 0.1);
	}

	.dropdown-item:hover .dropdown-label {
		color: var(--color-primary);
	}

	.dropdown-item:hover .dropdown-chevron {
		opacity: 1;
		transform: translateX(0);
		color: var(--color-primary);
	}

	.dropdown-icon {
		flex-shrink: 0;
		display: flex;
		align-items: center;
		justify-content: center;
		width: 36px;
		height: 36px;
		border-radius: 9px;
		background: var(--color-light);
		color: var(--color-body);
		transition: all 0.15s ease;
	}

	.dropdown-icon svg {
		width: 18px;
		height: 18px;
	}

	.dropdown-label {
		display: block;
		font-size: 13px;
		font-weight: 600;
		color: var(--color-dark);
		line-height: 1.3;
		transition: color 0.15s ease;
	}

	.dropdown-desc {
		display: block;
		font-size: 12px;
		color: var(--color-slate);
		line-height: 1.3;
		margin-top: 1px;
	}

	.dropdown-chevron {
		margin-left: auto;
		font-size: 14px;
		font-weight: 600;
		opacity: 0;
		transform: translateX(-4px);
		transition: all 0.15s ease;
		flex-shrink: 0;
	}

	@keyframes dropdown-in {
		from {
			opacity: 0;
			transform: translateX(-50%) translateY(4px) scale(0.97);
		}
		to {
			opacity: 1;
			transform: translateX(-50%) translateY(0) scale(1);
		}
	}

	@keyframes item-in {
		from {
			opacity: 0;
			transform: translateX(-6px);
		}
		to {
			opacity: 1;
			transform: translateX(0);
		}
	}
</style>
