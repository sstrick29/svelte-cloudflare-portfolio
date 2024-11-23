<script>
	import { page } from '$app/stores';
	import { onMount } from 'svelte';

	let { children } = $props();

	let seconds = $state(0);

	onMount(() => {
		const interval = setInterval(() => {
			seconds += 1;
		}, 1000);

		return () => {
			clearInterval(interval);
		};
	});
</script>

<nav>
	<a href="/">home</a>
	<a href="/about">about</a>
	<a href="/how">how</a>

	{#if $page.data.component}
		{@const Component = $page.data.component}
		<Component />
	{/if}
	
</nav>

{@render children()}

<p>You've been here for {seconds} seconds</p>