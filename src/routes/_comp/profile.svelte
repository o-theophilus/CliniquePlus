<section>
	<div class="block">
		<div class="a">
			<img src="/images/pic.png" alt="logo" />
			Isaac Isaac
		</div>
		<div class="hr" />
		<div class="b">
			<button>Change Password</button>
			<button class="btn2">Edit</button>
		</div>
		<div class="c">
			<div>
				<p>Staff ID</p>
				<p>1234</p>
			</div>
			<div>
				<p>Role</p>
				<p>Admin</p>
			</div>
			<div>
				<p>Designation</p>
				<p>CMD</p>
			</div>
			<div>
				<p>Department</p>
				<p>4</p>
			</div>
		</div>
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;

		padding: var(--gap2);
		padding-bottom: 0;
	}

	.block {
		box-shadow: var(--shad1);
		width: 100%;

		background-color: var(--clr2);
		border-radius: var(--brad1);

		overflow: hidden;
	}

	.a {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: var(--gap2);

		padding: var(--gap2);

		font-size: 1.5em;
		font-weight: bold;
		color: var(--clr3);
	}

	.b {
		display: flex;
		gap: var(--gap2);

		padding: var(--gap2);
		padding-bottom: 0;
		width: 100%;
	}
	button {
		padding: 0 var(--gap3);
		height: 40px;
		width: 100%;
		border-radius: var(--brad1);
		border: none;

		background: var(--clr3);
		color: var(--clr2);

		transition: all var(--animTime1) ease-in-out;
	}

	button:hover {
		background: var(--clr7);
	}
	.btn2 {
		width: unset;
		border: 1px solid var(--clr1);

		color: var(--clr1);
		background: var(--clr2);
	}
	.btn2:hover {
		background: var(--clr5);
	}

	.c {
		padding: var(--gap2);
	}
	.c div {
		display: flex;
		align-items: center;
		padding: 0 var(--gap2);

		padding: var(--gap2);

		gap: var(--gap2);
	}
	.c div p {
		width: 100%;
	}
	.c div:nth-child(odd) {
		background-color: var(--clr6);
	}

	.hr {
		height: 1px;
		margin: 0 var(--gap2);

		background-color: var(--clr4);
	}
</style>
