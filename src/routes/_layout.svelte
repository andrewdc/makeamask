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

:global(h1, h2, h3, h4, h5, h6) {
	font-family: alegreya, serif;
font-style: normal;
font-weight: 400;
}
	main {
		position: relative;
		background-color: none;
		padding: 2em;
		box-sizing: border-box;
		overflow-y:auto;
	}
	.content {
		margin: 0 auto;
		max-width: 56em;
		flex:1 0 auto;
	}
</style>

<Nav {segment}/>

<main>
<div class="content">
	<slot></slot>
	</div>

</main>