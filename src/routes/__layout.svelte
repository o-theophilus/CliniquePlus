<script>
	import '$lib/style/var.css';
	import '$lib/style/main.css';

	import { showNav, isMobile } from '$lib/store.js';

	let innerWidth;
	$: $isMobile = innerWidth < 900;
	// $: $showNav = !$isMobile ? false : $showNav;
</script>

<svelte:window bind:innerWidth />

<slot />
