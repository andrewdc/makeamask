<script>
let slotContent = ""

let printCard = function() {
	let printContents = slotContent.innerHTML;
	 let originalContents = document.body.innerHTML;

     document.body.innerHTML = printContents;

     window.print();
	
					location.reload();
}
</script>

<style>
	.contact-card {
		position:relative;
		flex:0 0 40%;
		background:#fff;
		border: 1px solid #aaa;
		border-radius: 2px;
		box-shadow: 2px 2px 8px rgba(0,0,0,0.1);
		padding: 1em;
		min-height:150px;;
		margin:0 8px;
	transition:all 0.15s ease-in-out;
	box-shadow:0 0 0 0 rgba(0, 0, 0, 0.0);
	}
		.contact-card:hover {
			box-shadow:0 0 3px 2px #55b9f3;
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

	.print-trigger {
		position: absolute;
    bottom: -8px;
    right: 5%;
				padding:0.5em;
				border:1px solid #55b9f3;
				background:#fff;
				border-radius:2px;
	}
	.print-trigger:hover {
		cursor:pointer;
	}

@media print {
	h2 {display:none;
	}
	.name {
				padding: 0 0 0.2em 0;
				font-size:1.2em;
				margin: 0 0 1em 0;
				border-bottom: 1px solid #55b9f3;
				color:#000;

	}
	.address {
		color:#000;
	}
  .card {
			width:400px;
			padding:2em;
			background:#fff;
		border: 1px solid #aaa;
		border-radius: 2px;
		box-shadow: 2px 2px 8px rgba(0,0,0,0.1);
		color:#000;

		}
		.print-trigger {display:none;}
}


</style>

<article class="contact-card" bind:this={slotContent}>
<div class="card">
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

	</div>
		<button class="print-trigger" href on:click|preventDefault={printCard}>Print Label</button>
</article>