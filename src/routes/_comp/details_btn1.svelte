<div>
	<button class=" active">Profile</button>
	<button>Payroll</button>
	<button>Leave</button>
	<button>Attendanc</button>
	<button>Document</button>
	<button>Timeline</button>
</div>

<style>
	div {
		--height: 40px;

		display: flex;
		gap: var(--gap2);

		padding: var(--gap2);
		width: 100%;
	}
	button {
		height: var(--height);
		padding: 0 var(--gap3);
		border: none;
		border-radius: var(--height);

		color: var(--clr1);
		background: var(--clr2);
		box-shadow: var(--shad1);
	}
	.active {
		color: var(--clr2);
		background: var(--clr3);
	}
</style>
