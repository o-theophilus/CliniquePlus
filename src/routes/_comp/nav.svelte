<script>
	import { showNav, isMobile } from '$lib/store.js';

	import SVG from '$lib/svg.svelte';

	const nav = () => {
		if ($isMobile) {
			$showNav = !$showNav;
		}
	};

	let showsub = true;
</script>

<nav class:showNav={$showNav}>
	<div class="bar">
		<div
			class="btn close"
			on:click={() => {
				$showNav = !$showNav;
			}}
		>
			<SVG type="close" size="16" />
		</div>
	</div>

	<div class="logo">
		<img src="/images/logo.png" alt="logo" />
		CliniqePlus
	</div>

	<div class="hr" />

	<div class="navArea">
		<div class="item active" on:click={nav}>
			<div class="left">
				<div class="svg">
					<SVG type="stack" size="16" />
				</div>

				Bed Status
			</div>
			<div class="right">
				<SVG type="angle" size="16" />
			</div>
		</div>

		<div class="item link" on:click={nav}>
			<div class="left">
				<div class="svg">
					<SVG type="portfolio" size="16" />
				</div>

				Front Office
			</div>
			<div class="right">
				<SVG type="angle" size="16" />
			</div>
		</div>

		<div class="item link" on:click={nav}>
			<div class="left">
				<div class="svg">
					<SVG type="stethoscope" size="16" />
				</div>

				HIS
			</div>
			<div class="right">
				<SVG type="angle" size="16" />
			</div>
		</div>

		<div class="item link" on:click={nav}>
			<div class="left">
				<div class="svg">
					<SVG type="drop" size="16" />
				</div>

				Blood Bank
			</div>
			<div class="right">
				<SVG type="angle" size="16" />
			</div>
		</div>
		<div
			class="item link"
			on:click={() => {
				showsub = !showsub;
			}}
		>
			<div class="left">
				<div class="svg">
					<SVG type="globe" size="16" />
				</div>

				LIS
			</div>
			<div class="right" class:showsub>
				<SVG type="angle" size="16" />
			</div>
		</div>

		<div class="sub" class:showsub>
			<div class="sub_ent" on:click={nav}>Order</div>
			<div class="sub_ent" on:click={nav}>QC</div>
			<div class="sub_ent" on:click={nav}>Phleb</div>
			<div class="sub_ent" on:click={nav}>Analysers</div>
		</div>

		<div class="item link" on:click={nav}>
			<div class="left">
				<div class="svg">
					<SVG type="chat" size="16" />
				</div>

				RIS
			</div>
			<div class="right">
				<SVG type="angle" size="16" />
			</div>
		</div>
		<div class="item link" on:click={nav}>
			<div class="left">
				<div class="svg">
					<SVG type="heart" size="16" />
				</div>

				Insurance
			</div>
			<div class="right">
				<SVG type="angle" size="16" />
			</div>
		</div>
	</div>
</nav>

<style>
	nav {
		display: none;
		position: fixed;

		z-index: 1;

		padding: var(--gap3);

		background-color: var(--clr2);

		inset: 0;

		box-shadow: var(--shad1);
	}
	@media screen and (min-width: 800px) {
		nav {
			position: static;
			width: 350px;
			flex-shrink: 0;
			flex-grow: 0;
		}
	}
	.showNav {
		display: block;
	}

	.bar {
		--size: 48px;
		display: flex;
		justify-content: right;
	}

	.close {
		display: flex;
		align-items: center;
		justify-content: center;

		width: var(--size);
		height: var(--size);
		padding: var(--gap2);

		border-radius: 50%;

		transition: all var(--animTime1) ease-in-out;
	}

	.close:hover {
		background-color: var(--clr6);
	}

	.logo {
		display: flex;
		align-items: center;
		justify-content: center;
		gap: var(--gap2);

		padding: var(--gap2);

		font-weight: 900;
		font-size: 1.3rem;
	}
	img {
		border-radius: 50%;
	}

	.item {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: var(--gap2);

		width: 100%;
		padding: var(--gap2);

		border-radius: var(--brad1);

		transition: all var(--animTime1) ease-in-out;
	}

	.item:hover {
		background-color: var(--clr6);
	}

	.active {
		background-color: var(--clr3);

		border-radius: 50px var(--brad1) var(--brad1) 50px;

		fill: var(--clr2);
		color: var(--clr2);
	}
	.active:hover {
		background-color: var(--clr7);
	}

	.left {
		display: flex;
		align-items: center;
		gap: var(--gap2);
	}
	.right {
		transform: rotate(90deg);

		transition: all var(--animTime2) ease-in-out;
	}
	.right.showsub {
		transform: rotate(180deg);
	}
	.hr {
		width: 100%;
		height: 1px;
		margin: var(--gap2) 0;

		background-color: var(--clr4);
	}

	.sub {
		display: none;

	}
	.showsub {
		display: block;
	}
	.sub_ent {
		padding: var(--gap2);
		padding-left: var(--gap5);
		background-color: var(--clr5);
		
		border-radius: var(--brad1);
		transition: all var(--animTime1) ease-in-out;
	}
	.sub_ent:hover {
		background-color: var(--clr6);
	}
</style>
