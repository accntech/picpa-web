<script lang="ts">
	import type { Snippet } from 'svelte';

	let {
		children,
		delay = 0,
		direction = 'up'
	}: {
		children: Snippet;
		delay?: number;
		direction?: 'up' | 'left' | 'right';
	} = $props();

	let visible = $state(false);

	function reveal(node: HTMLElement) {
		const observer = new IntersectionObserver(
			([entry]) => {
				if (entry.isIntersecting) {
					visible = true;
					observer.disconnect();
				}
			},
			{ threshold: 0.1 }
		);
		observer.observe(node);
		return { destroy: () => observer.disconnect() };
	}

	const transforms: Record<string, string> = {
		up: 'translateY(30px)',
		left: 'translateX(-30px)',
		right: 'translateX(30px)'
	};
</script>

<div
	use:reveal
	style="opacity: {visible ? 1 : 0}; transform: {visible ? 'none' : transforms[direction]}; transition: opacity 0.6s ease-out {delay}ms, transform 0.6s ease-out {delay}ms;"
>
	{@render children()}
</div>
