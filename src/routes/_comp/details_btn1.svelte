<div>
	<button class=" active">Profile</button>
	<button>Payroll</button>
	<button>Leave</button>
	<button>Attendance</button>
	<button>Document</button>
	<button>Timeline</button>
</div>

<style>
	div {
		--height: 40px;

		display: flex;
		flex-wrap: wrap;
		gap: var(--gap2);

		padding: var(--gap2);
		width: 100%;

		overflow-x: auto;
	}
	button {
		height: var(--height);
		padding: 0 var(--gap3);
		border: none;
		border-radius: var(--height);

		color: var(--clr1);
		background: var(--clr2);
		box-shadow: var(--shad1);

		transition: all var(--animTime1) ease-in-out;
	}

	button:hover {
		background: var(--clr6);
	}

	.active {
		color: var(--clr2);
		background: var(--clr3);
	}
	.active:hover {
		background: var(--clr7);
	}
</style>
