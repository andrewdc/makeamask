<style>
	.media-card {
		flex:0 0 auto;
		background:#fff;
		border: 1px solid #aaa;
		border-radius: 2px;
		box-shadow: 2px 2px 8px rgba(0,0,0,0.1);
		padding: 1em;
		min-height:150px;
		margin:0 8px 8px 8px;
	transition:all 0.15s ease-in-out;
	word-break:break-all;
	}
	.media-card:hover {
		box-shadow: 0 0 6px 4px rgba(46, 147, 254, 0.4)
	}

	h2 {
		font-size:1.8em;
		padding: 0 0 0.2em 0;
		margin: 0 0 1em 0;
		border-bottom: 1px solid #55b9f3;
	}

	.email, .twitter, .facebook, .link {
		padding: 0 0 0 1.8em;
		background:  0 0 no-repeat;
		background-size: 20px 20px;
		margin: 0 0 0.5em 0;
		line-height: 1.4em;
	}

 .email {background-image: url(/email.svg);}
 .twitter {background-image: url(/twitter.svg);}
 .facebook {background-image: url(/facebook.svg);}
 .link {background-image: url(/link.svg);}
</style>

<article class="media-card">
	<h2>
		<slot name="title">
		</slot>
	</h2>
<div class="link">
 <slot name="link">
 </slot>
</div>
<div class="email">
 <slot name="email">
 </slot>
</div>

	<div class="facebook">
		<slot name="facebook">
		</slot>
	</div>
	<div class="twitter">
		<slot name="twitter">
		</slot>
	</div>
	<div class="special">
		<slot name="special">
		</slot>
	</div>
</article>