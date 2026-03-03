<script lang="ts">
	let { image, date, title, excerpt }: {
		image: string;
		date: string;
		title: string;
		excerpt: string;
	} = $props();
</script>

<article class="overflow-hidden rounded-xl bg-white shadow-md transition-shadow hover:shadow-xl">
	<img src={image} alt={title} class="aspect-video w-full object-cover" />
	<div class="p-5">
		<p class="text-xs font-medium uppercase text-primary">{date}</p>
		<h3 class="mt-2 line-clamp-2 font-heading text-lg font-semibold text-dark">{title}</h3>
		<p class="mt-2 line-clamp-3 text-sm text-body">{excerpt}</p>
	</div>
</article>
