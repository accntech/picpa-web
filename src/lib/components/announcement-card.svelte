<script lang="ts">
	let { image, date, title, excerpt }: {
		image: string;
		date: string;
		title: string;
		excerpt: string;
	} = $props();
</script>

<article class="group relative overflow-hidden rounded-2xl bg-navy">
	<div class="aspect-[4/3] overflow-hidden">
		<img
			src={image}
			alt={title}
			class="h-full w-full object-cover transition-transform duration-500 group-hover:scale-110"
		/>
	</div>
	<div class="absolute inset-0 bg-linear-to-t from-navy via-navy/60 to-transparent"></div>
	<div class="absolute inset-x-0 bottom-0 p-6">
		<p class="text-xs font-medium uppercase tracking-widest text-primary">{date}</p>
		<h3 class="mt-2 font-heading text-lg font-bold leading-snug text-white">{title}</h3>
		<p class="mt-2 line-clamp-2 text-sm text-slate opacity-0 transition-opacity duration-300 group-hover:opacity-100">
			{excerpt}
		</p>
	</div>
</article>
