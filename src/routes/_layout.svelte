<script>
	import Nav from '../components/Nav.svelte';
	import Footer from '../components/Footer.svelte';
	import Button from '../components/Button.svelte';

	export let segment;
</script>

<style>
:global(a) {
	color:rgb(2, 110, 172);
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
		background-color:#f0f0f0;
		padding: 2em 10em;
		box-sizing: border-box;
		display:flex;
		max-width:100vw;
			min-height: 100vh;
			 /* put on top */
  position: relative;
  z-index: 1;
	}
	.facebook {
		flex:0 0 340px;
	}
	.content {
		margin: 0 auto;
		padding:0 3em;
		flex:1 1 100%;
	}
	@media (max-width: 978px) {
		.content {
			padding:0 1em;
		}
		main {
			flex-direction:column;
			padding:0em;
		}
	.faq {
		display:none;
		position: fixed;
    z-index: 1000;
    right: 1%;
    bottom: 1%;
				font-size:0.8em;
	}
	.facebook {
			flex:0 0 100%;
			display:flex;
			flex-direction: column;
			align-items:center;
			padding:1em 0.4em;
	}
	}
	 @media (min-width: 480px) {
   main {
      font-size: 1em;
    }

		}
		 @media (min-width: 320px) {
   main {
						padding: 0em;
    }
  }

		@media (max-width: 510px) {
		.content {
			padding:1em 0.4em;
		}
		.facebook {
			flex:0 0 100%;
			display:flex;
			flex-direction: column;
			align-items:stretch;
			padding:1em 0.4em;
		}
		}
			@media (min-width:1224px) {
		main {
			padding:2em 12%;
		}
	}
.group {border-radius:3px; width:100%; max-width:340px;}

</style>


<Nav {segment}/>
<main>

<div class="content">
	<slot></slot>
	</div>
<div class="facebook">
<div class="faq">
	<Button href="/#faq">
		<span slot="text">Jump to FAQ</span>
		<img slot="icon" src="/icons/001-brooch.svg" style="width:50px;transform:rotate(-90deg);" alt="mask" />
	</Button>
	</div>
	<h3>Join the Facebook Group</h3>
<a rel="noreferrer" target="_blank" href="https://www.facebook.com/groups/caremaskcoversforcovid19/">
<img class="group" src="/group.jpg" alt="Care Mask Covers for COVID-19 Facebook Group" />
</a>

		<h3>Like the Facebook Page</h3>

	<div class="fb-page" data-href="https://www.facebook.com/MakeAMask/" data-tabs="timeline, messages" data-width="" data-height="" data-small-header="false" data-adapt-container-width="true" data-hide-cover="false" data-show-facepile="true"><blockquote cite="https://www.facebook.com/MakeAMask/" class="fb-xfbml-parse-ignore"><a href="https://www.facebook.com/MakeAMask/">Make-A-Mask</a></blockquote></div>

			<h3>Say hello on Twitter</h3>
		<a href="https://twitter.com/intent/tweet?button_hashtag=MakeAMaskSewers&ref_src=twsrc%5Etfw" class="twitter-hashtag-button" data-size="large" data-related="Make-A-Mas" data-dnt="true" data-show-count="false">Tweet #MakeAMaskSewers</a><script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
	</div>
	<div>

</div>
</main>

<Footer></Footer>