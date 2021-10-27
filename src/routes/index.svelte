<script>
	import Header from './_comp/titleBar.svelte';
	import SearchBar from './_comp/searchBar.svelte';
	import Profile from './_comp/profile.svelte';
	import Details from './_comp/details.svelte';
	import Footer from './_comp/footer.svelte';

	import Nav from './_comp/nav.svelte';
</script>
	<svelte:head>
		<title>
			CliniquePlus
		</title>
	</svelte:head>

<main>
	<div class="content">
		<Nav />
		<div class="details">
			<Header />
			<SearchBar />
			<Profile />
			<Details />
		</div>
	</div>
	<Footer />
</main>

<style>
	main {
		background-color: var(--clr5);
		position: relative;
	}

	.content {
		display: flex;
	}
	.details {
		width: 100%;
	}
	/* @media screen and (min-width: 800px) {
	} */
</style>
