<script>
 import Button from "../components/Button.svelte";
 import Faq from "../components/Faq.svelte";
 import MediaLinks from "../components/MediaLinks.svelte";
  import { onMount } from "svelte";
    const COL_COUNT = 2; // set this to however many columns you want
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

<style lang="scss">
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
@media (max-width:510px){
  .buttons {
    flex-direction: column;
    align-items: initial;
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
  Help keep our Healthcare workers in the Austin, TX area safe! They are in dire need of Personal Protective Equipment, especially masks, for their safety. All masks are being donated.
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

<div class="fb-video" data-href="https://www.facebook.com/MakeAMask/videos/2646230642370048/" data-show-text="false" data-width=""><blockquote cite="https://developers.facebook.com/MakeAMask/videos/2646230642370048/" class="fb-xfbml-parse-ignore"><a href="https://developers.facebook.com/MakeAMask/videos/2646230642370048/">Thank you!!! Almost 10,000 Masks Donated!</a><p>These are just some of the facilities that are saying, “THANK YOU SO MUCH!!!” for their precious mask covers / face shields!! ❤️🙏😷🎉

How can you jump on the Make-A-Mask Movement?
We still have SOOO many requests left to fill!!

www.makeamaskaustin.org
www.instagram.com/makeamaskatx/</p>Posted by <a href="https://www.facebook.com/MakeAMask/">Make-A-Mask</a> on Tuesday, April 21, 2020</blockquote></div>

<h2>In the News</h2>

<MediaLinks></MediaLinks>

<Faq></Faq>