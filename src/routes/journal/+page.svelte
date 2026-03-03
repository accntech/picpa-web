<script lang="ts">
	import PageHero from '$lib/components/PageHero.svelte';

	const focusAreas = [
		{
			title: 'Philippine Accountancy Profession',
			desc: 'Research on the current state, challenges, and future direction of the accountancy profession in the Philippines.'
		},
		{
			title: 'Financial Reporting Standards',
			desc: 'Analysis and commentary on Philippine Financial Reporting Standards and their application.'
		},
		{
			title: 'Auditing & Assurance',
			desc: 'Studies on auditing practices, methodologies, and quality assurance in the Philippine context.'
		},
		{
			title: 'Taxation & Regulatory Compliance',
			desc: 'Research on Philippine tax regulations, compliance issues, and policy implications.'
		}
	];

	const articles = [
		{
			title: 'The Philippine Accountancy Profession Research Agenda',
			authors: 'PICPA Research Committee',
			year: '2024',
			abstract: 'A comprehensive research agenda outlining priority areas for academic and professional investigation in Philippine accountancy.'
		},
		{
			title: 'Impact of Digital Transformation on Audit Quality',
			authors: 'Various Contributors',
			year: '2023',
			abstract: 'An examination of how emerging technologies are reshaping audit methodologies and their implications for audit quality in the Philippines.'
		},
		{
			title: 'Sustainability Reporting Practices Among Philippine Listed Companies',
			authors: 'PICPA Foundation Research Team',
			year: '2023',
			abstract: 'A study analyzing the current state of sustainability reporting practices among publicly listed companies in the Philippines.'
		}
	];
</script>

<PageHero title="PICPA Journal" breadcrumbs={[{ label: 'Home', href: '/' }, { label: 'Journal' }]} />

<section class="bg-white py-20">
	<div class="mx-auto max-w-4xl px-4 text-center">
		<h2 class="font-heading text-3xl font-bold text-dark">Official Research Publication</h2>
		<p class="mt-4 leading-relaxed text-body">
			The PICPA Journal is the official research publication of the Philippine Institute of Certified
			Public Accountants. It serves as a platform for scholarly research, professional insights, and
			thought leadership in the field of accountancy.
		</p>
		<div class="mx-auto mt-8 h-1 w-20 bg-primary"></div>
	</div>
</section>

<section class="bg-light py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="text-center font-heading text-2xl font-bold text-dark">Research Focus Areas</h2>
		<div class="mt-8 grid grid-cols-1 gap-6 md:grid-cols-2">
			{#each focusAreas as area (area.title)}
				<div class="rounded-xl bg-white p-6">
					<h3 class="font-heading text-lg font-bold text-dark">{area.title}</h3>
					<p class="mt-2 text-sm text-body">{area.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-4">
		<h2 class="font-heading text-2xl font-bold text-dark">Published Articles</h2>
		<div class="mt-8 space-y-6">
			{#each articles as article (article.title)}
				<div class="flex flex-col gap-6 rounded-xl bg-light p-6 lg:flex-row">
					<div class="shrink-0 text-center lg:w-32">
						<div class="rounded-lg bg-primary/10 px-4 py-3 font-heading text-2xl font-bold text-primary">
							{article.year}
						</div>
					</div>
					<div>
						<h3 class="font-heading text-xl font-bold text-dark">{article.title}</h3>
						<p class="mt-1 text-sm text-primary">By {article.authors}</p>
						<p class="mt-2 text-body">{article.abstract}</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="bg-light py-16">
	<div class="mx-auto max-w-4xl px-4 text-center">
		<div class="rounded-2xl bg-white p-12 shadow-sm">
			<h2 class="font-heading text-2xl font-bold text-dark">Submit Your Research</h2>
			<p class="mt-4 text-body">
				The PICPA Journal welcomes submissions from CPAs, academics, and researchers. All articles
				undergo peer review to ensure quality and relevance.
			</p>
			<p class="mt-4 font-medium text-primary">
				For submission guidelines, contact: techsolutions@picpa.com.ph
			</p>
		</div>
	</div>
</section>
