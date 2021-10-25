<script>
	import SVG from '$lib/svg.svelte';
</script>

<div>
	<div class="btn"><SVG type="angle" size="16" /></div>
	Profile
	<div class="btn right"><SVG type="angle" size="16" /></div>
</div>

<style>
	div {
		--size: 48px;

		display: flex;
		justify-content: space-between;
		align-items: center;
		gap: var(--gap2);

		padding: var(--gap2);
		font-size: 1.2rem;
	}
	.btn {
		display: flex;
		justify-content: center;
		align-items: center;

		width: var(--size);
		height: var(--size);
		border: none;
		border-radius: var(--size);

		background: var(--clr2);
		box-shadow: var(--shad1);
		
		transform: rotate(-90deg);
	}

	.btn:hover{
		background: var(--clr3);
		fill: var(--clr2);

	}
	.right {
		transform: rotate(90deg);
	}
</style>
