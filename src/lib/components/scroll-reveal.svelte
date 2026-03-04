<script lang="ts">
	import type { Snippet } from 'svelte';

	let {
		children,
		class: className = '',
		delay = $bindable(0),
		direction = 'up',
		stagger = $bindable(0)
	}: {
		children: Snippet;
		class?: string;
		delay?: number;
		direction?: 'up' | 'left' | 'right' | 'down';
		stagger?: number;
	} = $props();

	let visible = $state(false);

	const totalDelay = delay + stagger * 80;

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
		up: 'translateY(40px)',
		down: 'translateY(-40px)',
		left: 'translateX(-40px)',
		right: 'translateX(40px)'
	};
</script>

<div
	class={className}
	use:reveal
	style="opacity: {visible ? 1 : 0}; filter: blur({visible ? 0 : 8}px); transform: {visible
		? 'none'
		: transforms[direction]}; transition: opacity 0.7s cubic-bezier(0.22, 1, 0.36, 1) {totalDelay}ms, filter 0.7s cubic-bezier(0.22, 1, 0.36, 1) {totalDelay}ms, transform 0.7s cubic-bezier(0.22, 1, 0.36, 1) {totalDelay}ms;"
>
	{@render children()}
</div>
