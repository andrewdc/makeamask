<style>
	.contact-card {
		flex:0 0 40%;
		background:#fff;
		border: 1px solid #aaa;
		border-radius: 2px;
		box-shadow: 2px 2px 8px rgba(0,0,0,0.1);
		padding: 1em;
		min-height:150px;;
		margin:0 8px;
	transition:all 0.15s ease-in-out;
	}
		.contact-card:hover {
			transform: scale(1.01);
		}

	h2 {
		padding: 0 0 0.2em 0;
		font-size:1.2em;
		margin: 0 0 1em 0;
		border-bottom: 1px solid #55b9f3;
	}

	.name, .address {
		padding: 0 0 0 1.5em;
		background:  0 0 no-repeat;
		background-size: 20px 20px;
		margin: 0 0 0.5em 0;
		line-height: 1.2;
	}

	.address { background-image: url(/map-marker.svg) }
	.name   { background-image: url(/user.svg);}
	.missing { color: #999 }
</style>

<article class="contact-card">
	<h2>
		<slot name="instruction">
			<span class="missing">SHIP TO:</span>
		</slot>
	</h2>

<div class="name">
<slot name="name">
	<span class="missing">nope</span>
</slot>
</div>

	<div class="address">
		<slot name="address">
			<span class="missing">Unknown address</span>
		</slot>
	</div>

	<!-- <div class="email">
		<slot name="email">
			<span class="missing">Unknown email</span>
		</slot>
	</div> -->
</article>