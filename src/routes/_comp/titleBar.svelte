<script>
	import TitleNav from './titleNav.svelte';
</script>

<header>
	<div class="logo link">
		<img src="/images/logo.png" alt="logo" />
		CliniqePlus
	</div>

	<TitleNav />
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 0 var(--gap2);

		height: 64px;

		background-color: var(--clr2);

		box-shadow: var(--shad1);
	}

	.logo {
		display: flex;
		align-items: center;
		gap: var(--gap2);

		font-weight: 900;
		font-size: 1.3rem;
	}
	@media screen and (min-width: 800px) {
		header {
			display: none;
		}
	}
</style>
