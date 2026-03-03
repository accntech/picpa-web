<script lang="ts">
	const stats = [
		{ icon: '/images/icons/employee.png', value: 196000, suffix: '+', label: 'CPAs in the Philippines' },
		{ icon: '/images/icons/chapters.png', value: 26000, suffix: '+', label: 'Active Members' },
		{ icon: '/images/icons/government.png', value: 84, suffix: '', label: 'Local Chapters' },
		{ icon: '/images/icons/international.png', value: 17, suffix: '', label: 'International Chapters' },
		{ icon: '/images/icons/school.png', value: 450, suffix: '+', label: 'Accredited Schools' }
	];

	let displayed = $state(stats.map(() => 0));

	function formatNumber(n: number): string {
		return Math.round(n).toLocaleString('en-US');
	}

	function animateCounters() {
		const duration = 2000;
		const start = performance.now();

		function tick(now: number) {
			const elapsed = now - start;
			const progress = Math.min(elapsed / duration, 1);
			const eased = 1 - Math.pow(1 - progress, 3);

			displayed = stats.map((s) => s.value * eased);

			if (progress < 1) {
				requestAnimationFrame(tick);
			}
		}

		requestAnimationFrame(tick);
	}

	function observe(node: HTMLElement) {
		let triggered = false;

		const observer = new IntersectionObserver(
			(entries) => {
				if (entries[0].isIntersecting && !triggered) {
					triggered = true;
					animateCounters();
				}
			},
			{ threshold: 0.2 }
		);

		observer.observe(node);

		return {
			destroy() {
				observer.disconnect();
			}
		};
	}
</script>

<section use:observe class="bg-light py-16">
	<div class="mx-auto grid max-w-7xl grid-cols-2 gap-8 px-4 text-center md:grid-cols-3 lg:grid-cols-5">
		{#each stats as stat, i (stat.label)}
			<div>
				<img src={stat.icon} alt={stat.label} class="mx-auto h-12 w-12" />
				<p class="mt-3 font-heading text-4xl font-bold text-primary">
					{formatNumber(displayed[i])}{stat.suffix}
				</p>
				<p class="mt-1 text-sm text-body">{stat.label}</p>
			</div>
		{/each}
	</div>
</section>
