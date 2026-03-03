<script lang="ts">
	import PageHero from '$lib/components/PageHero.svelte';

	const milestones = [
		{
			date: 'November 1929',
			text: 'PICPA was founded by eleven visionary CPAs: Enrique Caguiat, Santiago de la Cruz, Francisco Dalupan, Jaime Hernandez, Felipe Ollada, Ramon del Rosario, Antonio Sanchez, Jose Torres, Artemio Tulio, Clemente Uson, and Jesus Zulueta. W. W. Larkin, CPA Certificate No. 1, served as the first President.'
		},
		{
			date: '1973',
			text: 'Presidential Decree No. 223 officially recognized PICPA as the Accredited Integrated Professional Organization (AIPO) of Certified Public Accountants in the Philippines.'
		},
		{
			date: '2004',
			text: 'Republic Act No. 9298, the Philippine Accountancy Act of 2004, was enacted, further strengthening the regulatory framework for the accountancy profession.'
		},
		{
			date: 'Present',
			text: 'Today, PICPA represents over 196,000 CPAs with more than 26,000 active members, 84 local chapters, and 17 international chapters. PICPA has been awarded five times as PRC\'s most outstanding AIPO.'
		}
	];

	const goals = [
		{
			icon: '\u{1F4DC}',
			title: 'Regulate the Practice',
			desc: 'To regulate the practice of the accountancy profession in the Philippines'
		},
		{
			icon: '\u{1F4DA}',
			title: 'Advance Knowledge',
			desc: 'To advance the science of accountancy and promote higher professional standards'
		},
		{
			icon: '\u{1F91D}',
			title: 'Foster Collegiality',
			desc: 'To promote and maintain high professional and ethical standards among CPAs'
		},
		{
			icon: '\u{1F310}',
			title: 'Serve the Public',
			desc: 'To safeguard the interests of the public from unreliable financial reporting'
		}
	];

	const sectors = [
		{
			acronym: 'ACPAPP',
			title: 'Public Practice',
			desc: 'CPAs providing audit, tax, and advisory services to clients'
		},
		{
			acronym: 'ACPACI',
			title: 'Commerce & Industry',
			desc: 'CPAs employed in private businesses and corporations'
		},
		{
			acronym: 'nACPAE',
			title: 'Education/Academe',
			desc: 'CPAs in academic institutions and accounting education'
		},
		{
			acronym: 'GACPA',
			title: 'Government',
			desc: 'CPAs serving in government agencies and institutions'
		}
	];

	const stats = [
		{ number: '9', label: 'Regions Nationwide' },
		{ number: '21', label: 'Board Members' },
		{ number: '84', label: 'Local Chapters' }
	];
</script>

<PageHero title="About PICPA" breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'About' }]} />

<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-4">
		<div class="text-center">
			<h2 class="font-heading text-3xl font-bold text-dark">Our History</h2>
			<p class="mt-4 text-body">
				From humble beginnings to the premier CPA organization in the Philippines
			</p>
		</div>

		<div class="relative ml-4 mt-12 border-l-2 border-primary">
			{#each milestones as milestone (milestone.date)}
				<div class="relative pb-12 pl-8">
					<div
						class="absolute left-[-9px] top-0 h-4 w-4 rounded-full border-4 border-white bg-primary"
					></div>
					<p class="text-sm font-medium text-primary">{milestone.date}</p>
					<p class="mt-2 leading-relaxed text-body">{milestone.text}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4">
		<div class="text-center">
			<h2 class="font-heading text-3xl font-bold text-dark">Our Founding Goals</h2>
		</div>

		<div class="mt-12 grid grid-cols-1 gap-8 md:grid-cols-2">
			{#each goals as goal (goal.title)}
				<div class="rounded-xl bg-white p-8 shadow-sm">
					<span class="text-4xl">{goal.icon}</span>
					<h3 class="mt-4 font-heading text-xl font-bold text-dark">{goal.title}</h3>
					<p class="mt-2 text-body">{goal.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-4">
		<div class="text-center">
			<h2 class="font-heading text-3xl font-bold text-dark">Four Professional Sectors</h2>
			<p class="mt-4 text-body">
				PICPA members are organized into four key sectors of the profession
			</p>
		</div>

		<div class="mt-12 grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-4">
			{#each sectors as sector (sector.acronym)}
				<div
					class="rounded-xl border border-light bg-light p-6 text-center transition hover:border-primary/30"
				>
					<p class="text-xs font-medium uppercase tracking-wide text-primary">
						{sector.acronym}
					</p>
					<h3 class="mt-2 font-heading text-lg font-bold text-dark">{sector.title}</h3>
					<p class="mt-2 text-sm text-body">{sector.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4 text-center">
		<h2 class="font-heading text-3xl font-bold text-dark">Organizational Structure</h2>

		<div class="mx-auto mt-12 grid max-w-3xl grid-cols-3 gap-8">
			{#each stats as stat (stat.number)}
				<div>
					<p class="font-heading text-4xl font-bold text-primary">{stat.number}</p>
					<p class="mt-2 text-sm text-body">{stat.label}</p>
				</div>
			{/each}
		</div>

		<p class="mx-auto mt-8 max-w-2xl leading-relaxed text-body">
			PICPA's organizational structure spans 9 regions across the Philippines, governed by a
			21-member National Board of Directors, with 84 local chapters and 17 international
			chapters ensuring representation for all Filipino CPAs worldwide.
		</p>
	</div>
</section>
