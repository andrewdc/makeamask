<script>
 import Button from "../components/Button.svelte";
 import Faq from "../components/Faq.svelte";
  import { onMount } from "svelte";

  onMount(() => {
    if (window.netlifyIdentity) {
      window.netlifyIdentity.on("init", user => {
        if (!user) {
          window.netlifyIdentity.on("login", () => {
            document.location.href = "/admin/";
          });
        }
      });
    }
  });
</script>

<style>
  h1,
  p {
    text-align: left;
    margin: 0 auto;
  }

  h1 {
    font-size: 4em;
    text-transform: uppercase;
    font-weight: 700;
    margin: 0 0 0.5em 0;
  }

  p {
    margin: 1em auto;
  }
.buttons {
  display:flex;
  align-items:center;
  justify-content: stretch;
}
.quote {
  	font-family: alegreya, serif;
font-style: italic;
font-weight: 400;
font-size:2em;
  line-height: 1.2;
  color:rgb(74, 132, 157);
}
.media {
  /* display:flex;
  justify-content: center;
  flex-wrap: wrap; */
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(274px, 1fr));
    grid-gap: 10px;
    grid-auto-rows: minmax(180px, auto);
    grid-auto-flow: dense;
    padding: 10px;
}
/*iframe {
    padding: 1rem;
    font-size: 14px;
    font-weight: bold;
    border-radius: 5px;
} */
@media (max-width:510px){
  .buttons {
    flex-direction: column;
  }
}

	 @media (max-width: 890px) {
     h1 {
       font-size:3em;
     }
     .quote {
       font-size:1em;
     }
		}
   
</style>

<svelte:head>
  <title>Make A Mask</title>
    <meta name="Description" content="As a creator: Learn how to create masks, where to ship them. As a medical provider: how to request masks">
  <script src="https://identity.netlify.com/v1/netlify-identity-widget.js">

  </script>
</svelte:head>

<h1>Make a Mask</h1>

<p class="quote">
  Help keep our Healthcare workers in the Austin, TX area safe! They are in dire need of Personal Protective Equipment, especially masks, for their safety. These can’t be purchased through retailers.
</p>
<div class="buttons">


<Button href="providers">
  <img slot="icon" src="/icons/021-mask.svg" style="width:50px;" alt="mask" />
    <span slot="text">  Healthcare Providers</span>
</Button>


<Button href="creators">
  <img slot="icon" src="/icons/002-fashion.svg" style="width:50px;" alt="spool" />
    <span slot="text">  Mask Creators</span>
</Button>

</div>

<h2>In the News</h2>
<div class="media">

<iframe title="Las fundas de Telemundo Austin hacen una máscara" src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FOliviaMartinezTelemundoAustin%2Fposts%2F1927382870731139&width=auto" width="auto" height="636" style="border:none;overflow:hidden;flex:1 0 auto;border:none;overflow:hidden;width:100%;max-width:400px;" scrolling="no" frameborder="0" allowTransparency="true" allow="encrypted-media"></iframe>

<iframe title="Community Impact Story" src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FimpactnewsSWA%2Fposts%2F2804351129618793&width=auto" width="auto" height="636" style="border:none;overflow:hidden;flex:1 0 auto;border:none;overflow:hidden;width:100%;max-width:400px;" scrolling="no" frameborder="0" allowTransparency="true" allow="encrypted-media"></iframe>

<iframe title="kxan News Story" src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FKXANnews%2Fposts%2F10157585767123037&width=auto" width="auto" height="455" style="border:none;overflow:hidden;flex:1 0 auto;border:none;overflow:hidden;width:100%;max-width:400px;" scrolling="no" frameborder="0" allowTransparency="true" allow="encrypted-media"></iframe>

<iframe title="Fashionable Austin Story" src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FFashionablyAustin%2Fposts%2F10156885842750927&width=auto" width="auto" height="620" style="flex:1 0 auto;border:none;overflow:hidden;width:100%;max-width:400px;" scrolling="no" frameborder="0" allowTransparency="true" allow="encrypted-media"></iframe>

</div>

<Faq></Faq>