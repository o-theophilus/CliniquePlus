<script>
	import SVG from '$lib/svg.svelte';
	import ProfileMenu from './profileMenu.svelte';

	import { showProfileMenu } from '$lib/store.js';
</script>

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
		class="profile"
		id="title_user_btn"
		on:click={() => {
			$showProfileMenu = !$showProfileMenu;
		}}
	>
		<div class="btn user" />

		<div class="profile_extra">
			<div class="username">Samson Monday</div>
			<div class="btn" class:showProfileMenu={$showProfileMenu}>
				<SVG type="angle" size="16" />
			</div>
		</div>
	</div>

	<ProfileMenu />
</nav>

<style>
	nav {
		--size: 32px;

		position: relative;

		display: flex;
		align-items: center;
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

		flex-shrink: 0;

		transition: all var(--animTime1) ease-in-out;
	}
	.btn:hover {
		background-color: var(--clr6);
		box-shadow: 0 0 2px 10px var(--clr6);
		z-index: 1;
	}
	.user {
		background-image: url('/images/pic.png');
		background-size: cover;
	}

	.profile {
		/* width: 100%; */
		display: flex;
		align-items: center;
		gap: var(--gap1);

		cursor: pointer;
	}

	.profile * {
		pointer-events: none;
	}

	.profile_extra {
		display: none;
		align-items: center;
		gap: var(--gap1);

		font-weight: 700;
	}

	.username {
		font-size: 0.7rem;
	}
	@media screen and (min-width: 800px) {
		.profile_extra {
			display: flex;
		}
	}

	.profile_extra .btn {
		transition: all var(--animTime3) ease-in-out;
	}
	.profile_extra .showProfileMenu {
		transform: rotate(180deg);
	}
</style>
