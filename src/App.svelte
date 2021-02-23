<script>
	import Board from './Board.svelte';
	export let name;
</script>

<main>
	<h1>Chess</h1>
	<Board />
</main>

<style>
	main {
		text-align: center;
		/* padding: 0 0.25rem; */
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4rem;
		font-weight: 100;
	}

	/* @media (min-width: 640px) {
		main {
			max-width: none;
		}
	} */
</style>