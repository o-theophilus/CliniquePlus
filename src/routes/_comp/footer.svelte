<footer>
	<div>CliniquePlus EMR by Netwalkers NG © 2021. All right reserved.</div>
	<div class="a">
		<div>About Us</div>
		<div class="vr" />
		<div>Contact Us</div>
		<div class="vr" />
		<div>Terms Of Service</div>
		<div class="vr" />
		<div>Privacy Policy</div>
	</div>
</footer>

<style>
	footer {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		gap: var(--gap2);

		padding: var(--gap2);

		background-color: white;
		box-shadow: var(--shad1);

		font-size: 0.8em;
		text-align: center;
	}
	@media screen and (min-width: 900px) {
		footer {
			flex-direction: row;
			height: 100%;
		}
	}
	.a {
		display: flex;
		gap: var(--gap2);
		flex-shrink: 0;
	}

	.vr {
		width: 1px;
		height: 24px;

		background-color: var(--clr4);
	}
</style>
