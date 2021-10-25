<script>
	import B1 from './details_btn1.svelte';
	import B2 from './details_btn2.svelte';

	var isMobile = true;
</script>

<section>
	<div class="block">
		<div class="a">HR / Staff Profile</div>
		<div class="hr" />
		{#if isMobile}
			<B2 />
		{:else}
			<B1 />
		{/if}

		<div class="hr" />
		<div class="c">
			<div>
				<p>Phone</p>
				<p>+23480 1234 567</p>
			</div>
			<div>
				<p>Emergency Contact</p>
				<p>+23480 7654 321</p>
			</div>
			<div>
				<p>Email</p>
				<p>isaacisaac@gmail.com</p>
			</div>
			<div>
				<p>Date of Birth</p>
				<p>14-10-1991</p>
			</div>
			<div>
				<p>Speciality</p>
				<p>1</p>
			</div>
			<div>
				<p>Father Name</p>
				<p>Edwin Isaac</p>
			</div>
			<div>
				<p>Mother Median Name</p>
				<p>Loveth John</p>
			</div>
			<div>
				<p>Highest Qualification</p>
				<p>B.Eng</p>
			</div>
			<div>
				<p>Qualification Date</p>
				<p>2015</p>
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
	}

	.block {
		width: 100%;
		border-radius: var(--brad1);

		background-color: var(--clr2);
		box-shadow: var(--shad1);

		overflow: hidden;
	}

	.a {
		padding: var(--gap2);
	}

	.c {
		padding: var(--gap2);
	}

	.c div {
		display: flex;
		align-items: center;
		gap: var(--gap2);

		padding: var(--gap2);
	}

	.c div p {
		width: 100%;
	}
	.c div p:nth-child(2) {
		text-align: right;
	}
	.c div:nth-child(odd) {
		background-color: var(--clr6);
	}

	.hr {
		height: 1px;

		background-color: var(--clr4);
	}
</style>
