<script>
	import { showNav } from '$lib/store.js';

	import SVG from '$lib/svg.svelte';
	import TitleNav from './titleNav.svelte';
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

	<div class="titleNav">
		<TitleNav />
	</div>
</div>

<style>
	.bar {
		--size: 48px;

		position: relative;

		display: flex;
		align-items: center;

		padding: var(--gap2);
		padding-bottom: 0;
	}
	label {
		position: absolute;
		left: calc(var(--size) + (var(--gap2)) * 2);
		top: 32px;
	}

	.btn {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-shrink: 0;

		width: var(--size);
		height: var(--size);

		background: var(--clr5);

		border: 1px solid var(--clr4);

		transition: all var(--animTime1) ease-in-out;
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

		transition: all var(--animTime1) ease-in-out;
	}
	input:hover,
	input:focus {
		background: var(--clr2);
	}

	.titleNav {
		display: none;
		padding: 0 var(--gap2);
		border: 1px solid var(--clr4);
		border-left: none;

		height: var(--size);
	}
	@media screen and (min-width: 800px) {
		.titleNav {
			display: flex;
		}
	}
</style>
