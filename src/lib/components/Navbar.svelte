<script lang="ts">
	import MobileMenu from './mobile-menu.svelte';

	let { transparent = false }: { transparent?: boolean } = $props();

	let scrolled = $state(false);
	let mobileOpen = $state(false);
	let aboutOpen = $state(false);

	$effect(() => {
		function onScroll() {
			scrolled = window.scrollY > 50;
		}
		onScroll();
		window.addEventListener('scroll', onScroll, { passive: true });
		return () => window.removeEventListener('scroll', onScroll);
	});

	const navLinks = [
		{ label: 'Home', href: '/' },
		{
			label: 'About',
			href: '/about',
			children: [
				{ label: 'About PICPA', href: '/about' },
				{ label: 'Vision & Mission', href: '/about/vision-mission' },
				{ label: 'Officers', href: '/about/officers' },
				{ label: "President's Corner", href: '/about/presidents-corner' }
			]
		},
		{ label: 'Events', href: '/events' },
		{ label: 'Careers', href: '/careers' },
		{ label: 'Foundation', href: '/foundation' },
		{ label: 'Members', href: '/members' },
		{ label: 'Chapters', href: '/chapters' },
		{ label: 'Journal', href: '/journal' },
		{ label: 'Contact', href: '/contact' }
	];

	let isTransparent = $derived(transparent && !scrolled);
</script>

<header
	class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 {isTransparent
		? 'bg-transparent'
		: 'bg-white shadow-md'}"
>
	<nav class="mx-auto flex max-w-7xl items-center justify-between px-4 py-3 lg:px-8">
		<a href="/">
			<img
				src={isTransparent ? '/images/logos/light-logo.png' : '/images/logos/dark-logo.png'}
				alt="PICPA Logo"
				class="h-10"
			/>
		</a>

		<ul class="hidden items-center gap-1 lg:flex">
			{#each navLinks as link (link.href)}
				<li class="relative">
					{#if link.children}
						<button
							class="relative cursor-pointer px-3 py-2 text-sm font-medium transition-colors after:absolute after:bottom-0 after:left-3 after:right-3 after:h-0.5 after:origin-left after:scale-x-0 after:bg-primary after:transition-transform hover:text-primary hover:after:scale-x-100 {isTransparent
								? 'text-white'
								: 'text-dark'}"
							onmouseenter={() => (aboutOpen = true)}
							onmouseleave={() => (aboutOpen = false)}
						>
							{link.label}
							<svg
								class="ml-1 inline-block h-3 w-3 transition-transform {aboutOpen
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
						{#if aboutOpen}
							<!-- svelte-ignore a11y_no_static_element_interactions -->
							<div
								class="absolute left-0 top-full min-w-52 rounded-lg bg-white py-2 shadow-lg"
								onmouseenter={() => (aboutOpen = true)}
								onmouseleave={() => (aboutOpen = false)}
							>
								{#each link.children as child (child.href)}
									<a
										href={child.href}
										class="block px-4 py-2 text-sm text-dark transition-colors hover:bg-light hover:text-primary"
									>
										{child.label}
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
				class="rounded-lg bg-primary px-5 py-2.5 text-sm font-medium text-white transition-colors hover:bg-primary-dark"
			>
				My MELS Account
			</a>
		</div>

		<button
			class="cursor-pointer lg:hidden {isTransparent ? 'text-white' : 'text-dark'}"
			onclick={() => (mobileOpen = true)}
			aria-label="Open menu"
		>
			<svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
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
