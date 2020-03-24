<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style>
:global(a) {
	color:rgb(19, 153, 230);
}
:global(body) {
	background-color:#f0f0f0;
}
	main {
		position: relative;
		max-width: 56em;
		background-color: none;
		padding: 2em;
		margin: 0 auto;
		box-sizing: border-box;
	}
</style>

<Nav {segment}/>

<main>
	<slot></slot>
</main>