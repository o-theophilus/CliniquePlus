<script>
	import { showProfileMenu } from '$lib/store.js';

	import SVG from '$lib/svg.svelte';
</script>

<nav
	class:showProfileMenu={$showProfileMenu}
	on:click={() => {
		$showProfileMenu = false;
	}}
>
	<div class="username">Samson Monday</div>
	<div class="btn">
		<div class="svg">
			<SVG type="user" size="16" />
		</div>
		Profile Update & Manager
	</div>
	<div class="btn">
		<div class="svg">
			<SVG type="help" size="16" />
		</div>
		Help & Support Contact & FAQ
	</div>
	<div class="btn">
		<div class="svg">
			<SVG type="caution" size="16" />
		</div>
		Complaint Report Error
	</div>
	<div class="btn logout">
		<div>
			<SVG type="logout" size="16" />
		</div>
		Logout
	</div>
</nav>

<style>
	nav {
		display: none;

		position: absolute;
		z-index: 1;
		/* width: 500px; */

		box-shadow: var(--shad1);

		top: calc(100% + 10px);
		right: 0;

		border-radius: var(--brad1);
		overflow: hidden;
		background: var(--clr2);
	}

	.showProfileMenu {
		display: block;
	}

	.btn {
		display: flex;
		align-items: center;
		justify-content: center;
		gap: var(--gap2);

		padding: var(--gap1) var(--gap2);
		background: var(--clr2);
	}
	.btn:hover {
		background: var(--clr6);
	}
	.logout {
		color: var(--clr2);
		background: var(--clr3);
		fill: var(--clr2);
	}

	.logout:hover {
		background: var(--clr7);
	}

	.svg {
		--size: 32px;

		display: flex;
		justify-content: center;
		align-items: center;
		flex-shrink: 0;

		border-radius: 50%;
		border: 1px solid var(--clr4);

		width: var(--size);
		height: var(--size);

		fill: var(--clr3);
	}

	.username {
		padding: var(--gap1) var(--gap2);
		text-align: center;
		font-weight: 700;
	}
	@media screen and (min-width: 800px) {
		.username {
			display: none;
		}
	}
</style>
