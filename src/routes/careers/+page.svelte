<script lang="ts">
	import PageHero from '$lib/components/PageHero.svelte';
</script>

<PageHero title="Careers" breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'Careers' }]} />

<section class="bg-primary/5 py-8">
	<div class="mx-auto max-w-7xl px-4 text-center">
		<p class="font-body text-body">
			PICPA offers a free job posting service for accountancy-related positions. Listings are
			active for one month.
		</p>
	</div>
</section>

<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="font-heading text-2xl font-bold text-dark">Current Job Openings</h2>

		<div class="mt-8 space-y-6">
			<div class="flex flex-col items-start gap-6 rounded-xl bg-light p-6 lg:flex-row">
				<img
					src="/images/careers/hiring-poster.jpg"
					alt="Financial Analyst hiring poster"
					class="w-full shrink-0 rounded-lg object-cover lg:w-48"
				/>
				<div>
					<span
						class="inline-block rounded-full bg-primary/10 px-3 py-1 text-xs font-medium text-primary"
					>
						Active
					</span>
					<h3 class="mt-2 font-heading text-xl font-bold text-dark">Financial Analyst</h3>
					<p class="mt-1 text-body">Asian Hospital and Medical Center</p>
					<p class="mt-1 flex items-center gap-1 text-sm text-body">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							class="size-4"
							viewBox="0 0 24 24"
							fill="none"
							stroke="currentColor"
							stroke-width="2"
							stroke-linecap="round"
							stroke-linejoin="round"
						>
							<path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z" />
							<circle cx="12" cy="10" r="3" />
						</svg>
						Muntinlupa City, Metro Manila
					</p>
					<div class="mt-3 flex flex-wrap gap-2">
						<span class="rounded-full border bg-white px-3 py-1 text-xs text-body">
							Full-time
						</span>
						<span class="rounded-full border bg-white px-3 py-1 text-xs text-body">
							Finance
						</span>
						<span class="rounded-full border bg-white px-3 py-1 text-xs text-body">
							Entry-level
						</span>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="text-center font-heading text-2xl font-bold text-dark">
			Career Development Resources
		</h2>

		<div class="mt-12 grid grid-cols-1 gap-8 md:grid-cols-3">
			<div class="rounded-xl bg-white p-8 text-center shadow-sm">
				<div class="text-4xl">🎓</div>
				<h3 class="mt-4 font-heading text-lg font-bold text-dark">Becoming a CPA</h3>
				<p class="mt-2 text-sm text-body">
					Learn about the steps to becoming a licensed Certified Public Accountant in the
					Philippines, including education requirements and the CPA board exam.
				</p>
			</div>

			<div class="rounded-xl bg-white p-8 text-center shadow-sm">
				<div class="text-4xl">🌏</div>
				<h3 class="mt-4 font-heading text-lg font-bold text-dark">ASEAN CPA</h3>
				<p class="mt-2 text-sm text-body">
					Explore the ASEAN Mutual Recognition Arrangement that allows CPAs to practice
					across ASEAN member states.
				</p>
			</div>

			<div class="rounded-xl bg-white p-8 text-center shadow-sm">
				<div class="text-4xl">📋</div>
				<h3 class="mt-4 font-heading text-lg font-bold text-dark">CIA Challenge</h3>
				<p class="mt-2 text-sm text-body">
					Information about the Certified Internal Auditor certification and how Philippine
					CPAs can pursue this international credential.
				</p>
			</div>
		</div>
	</div>
</section>

<section class="bg-white py-16">
	<div class="mx-auto max-w-4xl px-4 text-center">
		<div class="rounded-2xl bg-primary/5 p-12">
			<h2 class="font-heading text-2xl font-bold text-dark">Want to Post a Job?</h2>
			<p class="mt-2 text-body">
				PICPA members and organizations can post accountancy-related job openings for free.
			</p>
			<p class="mt-4 font-medium text-primary">Email: membership@picpa.com.ph</p>
		</div>
	</div>
</section>
