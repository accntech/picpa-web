<script lang="ts">
	import PageHero from '$lib/components/PageHero.svelte';

	const programs = [
		{
			icon: '🔬',
			title: 'Research & Development',
			desc: 'Funding and supporting research initiatives that advance accounting knowledge and practice in the Philippines.'
		},
		{
			icon: '📈',
			title: 'Professional Development',
			desc: 'Programs designed to enhance the skills and competencies of Filipino CPAs across all sectors.'
		},
		{
			icon: '🎓',
			title: 'Scholarships',
			desc: 'Providing financial assistance to deserving accounting students to pursue their education and career goals.'
		},
		{
			icon: '🏫',
			title: 'Ayuda sa Escuela',
			desc: 'A community outreach program providing support to schools and educational institutions across the country.'
		}
	];

	const founders = [
		{ name: 'Jaime C. Laya', subtitle: 'Former BSP Governor' },
		{ name: 'Washington A. SyCip', subtitle: 'Founder, SGV & Co.' },
		{ name: 'Roberto Ongpin', subtitle: 'Business Leader' }
	];
</script>

<PageHero
	title="PICPA Foundation"
	breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'Foundation' }]}
/>

<section class="bg-white py-20">
	<div class="mx-auto grid max-w-7xl grid-cols-1 items-center gap-12 px-4 lg:grid-cols-2">
		<img
			src="/images/foundation/logo.jpg"
			alt="PICPA Foundation Logo"
			class="rounded-xl"
		/>
		<div>
			<span class="rounded-full bg-gold/10 px-4 py-1.5 text-sm font-medium text-gold">
				Established December 29, 1981
			</span>
			<h2 class="mt-4 font-heading text-3xl font-bold text-dark">PICPA Foundation Inc.</h2>
			<p class="mt-4 leading-relaxed text-body">
				The PICPA Foundation, Inc. was established to support the advancement of the accountancy
				profession in the Philippines through research, professional development, scholarships, and
				community service programs.
			</p>
			<p class="mt-3 text-body">
				The Foundation is accredited by the Philippine Council for NGO Certification (PCNC) and
				holds Donee Institution status, enabling it to receive tax-deductible donations.
			</p>
		</div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="text-center font-heading text-3xl font-bold text-dark">Our Programs</h2>
		<div class="mt-12 grid grid-cols-1 gap-8 md:grid-cols-2">
			{#each programs as program (program.title)}
				<div class="rounded-xl bg-white p-8 shadow-sm transition hover:shadow-md">
					<span class="text-4xl">{program.icon}</span>
					<h3 class="mt-4 font-heading text-xl font-bold text-dark">{program.title}</h3>
					<p class="mt-2 text-body">{program.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="bg-white py-20">
	<div class="mx-auto grid max-w-7xl grid-cols-1 items-center gap-12 px-4 lg:grid-cols-2">
		<div>
			<h2 class="font-heading text-3xl font-bold text-dark">Parangal San Mateo Awards</h2>
			<p class="mt-4 leading-relaxed text-body">
				The Parangal San Mateo Awards is the PICPA Foundation's premier recognition program,
				honoring outstanding CPAs who have made significant contributions to the accountancy
				profession and to society.
			</p>
			<p class="mt-3 text-body">
				Named after Saint Matthew, the patron saint of accountants, these awards celebrate
				excellence, integrity, and service.
			</p>
		</div>
		<img
			src="/images/foundation/parangal.png"
			alt="Parangal San Mateo Awards"
			class="mx-auto max-h-[500px] rounded-xl object-contain shadow-lg"
		/>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="text-center font-heading text-2xl font-bold text-dark">
			Recognition & Accreditation
		</h2>
		<div class="mx-auto mt-8 grid max-w-4xl grid-cols-1 gap-8 md:grid-cols-2">
			<div class="rounded-xl bg-white p-8 text-center">
				<h3 class="font-heading text-xl font-bold text-dark">PCNC Accredited</h3>
				<p class="mt-2 text-body">
					Accredited by the Philippine Council for NGO Certification, recognizing our adherence to
					the highest standards of non-profit governance.
				</p>
			</div>
			<div class="rounded-xl bg-white p-8 text-center">
				<h3 class="font-heading text-xl font-bold text-dark">Donee Institution</h3>
				<p class="mt-2 text-body">
					Granted Donee Institution status by the Bureau of Internal Revenue, enabling
					tax-deductible donations.
				</p>
			</div>
		</div>
		<div class="mt-8 text-center">
			<img
				src="/images/foundation/donee-certificate.png"
				alt="Donee Institution Certificate"
				class="mx-auto max-w-sm rounded-lg shadow-md"
			/>
		</div>
	</div>
</section>

<section class="bg-white py-20">
	<div class="mx-auto max-w-4xl px-4 text-center">
		<h2 class="font-heading text-2xl font-bold text-dark">Notable Founders</h2>
		<p class="mt-4 text-body">
			The PICPA Foundation was established through the vision of prominent Filipino leaders:
		</p>
		<div class="mt-8 grid grid-cols-1 gap-6 md:grid-cols-3">
			{#each founders as founder (founder.name)}
				<div class="rounded-xl bg-light p-6">
					<p class="font-heading text-lg font-bold text-dark">{founder.name}</p>
					<p class="mt-1 text-sm text-body">{founder.subtitle}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4 text-center">
		<h2 class="font-heading text-2xl font-bold text-dark">Board of Trustees</h2>
		<p class="mt-2 text-body">FY 2024-2025</p>
		<img
			src="/images/foundation/board.png"
			alt="PICPA Foundation Board of Trustees"
			class="mt-8 w-full rounded-2xl shadow-lg"
		/>
		<img
			src="/images/foundation/committee.png"
			alt="PICPA Foundation Committee Members"
			class="mt-8 w-full rounded-2xl shadow-lg"
		/>
		<p class="mt-4 text-sm text-body">
			PICPA Foundation Board of Trustees and Committee Members
		</p>
	</div>
</section>
