<script>
	import SVG from '$lib/svg.svelte';
	import ProfileMenu from './profileMenu.svelte';

	import { showProfileMenu } from '$lib/store.js';
</script>

<header>
	<div class="logo link">
		<img src="/images/logo.png" alt="logo" />
		CliniqePlus
	</div>

	<nav>
		<div class="btn">
			<SVG type="notification" size="16" />
		</div>
		<div class="btn">
			<SVG type="message" size="16" />
		</div>
		<div class="btn">
			<SVG type="expand" size="16" />
		</div>
		<div
			class="btn"
			on:click={() => {
				$showProfileMenu = !$showProfileMenu;
			}}
		>
			<img src="/images/pic.png" alt="logo" />
		</div>

		<ProfileMenu />
	</nav>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 0 var(--gap2);

		height: 64px;

		background-color: white;

		box-shadow: var(--shad1);
	}

	.logo {
		display: flex;
		align-items: center;
		gap: var(--gap2);

		font-weight: 900;
		font-size: 1.3rem;
	}
	img {
		border-radius: 50%;
	}
	nav {
		--size: 32px;

		position: relative;

		display: flex;
		gap: var(--gap1);
	}

	.btn {
		display: flex;
		justify-content: center;
		align-items: center;

		border-radius: 50%;
		background-color: var(--clr2);

		width: var(--size);
		height: var(--size);
	}
	.btn:hover {
		background-color: var(--clr6);
		box-shadow: 0 0 2px 10px var(--clr6);
		z-index: 1;
	}
	img {
		width: var(--size);
		height: var(--size);
	}
</style>
