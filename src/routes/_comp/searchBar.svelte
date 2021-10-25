<script>
	import { showNav } from '$lib/store.js';

	import SVG from '$lib/svg.svelte';
</script>

<div class="bar">
	<div
		class="btn"
		on:click={() => {
			$showNav = !$showNav;
		}}
	>
		<SVG type="menu" size="16" />
	</div>

	<label for="search">
		<SVG type="search" size="16" />
	</label>
	<input type="text" placeholder="Search for patient" id="search" />
</div>

<style>
	div {
		position: relative;
		--size: 48px;
		display: flex;
		padding: var(--gap2);
		padding-bottom: 0;
	}
	label {
		position: absolute;
		left: calc(var(--size) + (var(--gap2)) * 2);
		top: 32px;
	}

	.btn {
		width: var(--size);
		height: var(--size);
		flex-shrink: 0;

		background: var(--clr5);

		border: 1px solid var(--clr4);

		cursor: pointer;
	}
	.btn:hover {
		background: var(--clr3);

		fill: var(--clr2);
	}

	input {
		padding: 0px 24px 0 48px;

		position: static;
		width: 100%;
		height: var(--size);

		background: var(--clr5);

		border: 1px solid var(--clr4);
	}
	input:hover,
	input:focus {
		background: var(--clr2);
	}
</style>
