<script lang="ts">
	import PageHero from '$lib/components/PageHero.svelte';

	const coreValues = [
		{
			icon: '⭐',
			title: 'Professional Excellence',
			desc: 'Dedication to excellence across all areas of professional practice'
		},
		{
			icon: '🛡️',
			title: 'Integrity',
			desc: 'Truthfulness, honesty, uprightness, and sound moral principles'
		},
		{
			icon: '💪',
			title: 'Commitment',
			desc: 'Dedication to organizational ideals and PICPA objectives'
		},
		{
			icon: '🤝',
			title: 'Partnership & Team Work',
			desc: 'Unity, harmony, and collaborative spirit among members'
		},
		{
			icon: '✅',
			title: 'Advocacy for Quality',
			desc: 'Strict adherence to the code of professional conduct'
		},
		{
			icon: '💡',
			title: 'New Technologies & Innovativeness',
			desc: 'Continuous pursuit of creativity and technological advancement'
		},
		{
			icon: '🌍',
			title: 'Social Responsibility',
			desc: 'Active commitment to societal duty and community service'
		}
	];
</script>

<PageHero
	title="Vision & Mission"
	breadcrumbs={[
		{ label: 'Home', href: '/' },
		{ label: 'About', href: '/about' },
		{ label: 'Vision & Mission' }
	]}
/>

<section class="bg-white py-20">
	<div class="mx-auto max-w-4xl px-4 text-center">
		<p class="text-sm font-medium uppercase tracking-widest text-primary">Our Vision</p>
		<p class="font-serif text-6xl leading-none text-primary/20">&ldquo;</p>
		<p class="mt-2 font-heading text-2xl font-bold leading-relaxed text-dark lg:text-3xl">
			A responsive and globally relevant professional organization committed to service excellence
			towards its members and stakeholders.
		</p>
		<div class="mx-auto mt-8 h-1 w-20 bg-primary"></div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-4xl px-4 text-center">
		<p class="text-sm font-medium uppercase tracking-widest text-primary">Our Mission</p>
		<p class="mt-4 font-heading text-xl leading-relaxed text-dark lg:text-2xl">
			To serve the best interest of the members and the stakeholders while promoting, upholding,
			and maintaining high standards in the accountancy profession and protecting public interest.
		</p>
		<div class="mx-auto mt-8 h-1 w-20 bg-primary"></div>
	</div>
</section>

<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-4">
		<div class="text-center">
			<h2 class="font-heading text-3xl font-bold text-dark">Our Core Values</h2>
			<p class="mt-2 text-body">The principles that guide our organization</p>
		</div>

		<div class="mt-12 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each coreValues as value (value.title)}
				<div class="rounded-xl bg-light p-8 transition hover:shadow-md">
					<span class="text-3xl">{value.icon}</span>
					<h3 class="mt-4 font-heading text-lg font-bold text-dark">{value.title}</h3>
					<p class="mt-2 text-body">{value.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
