<script>
 import Button from "../components/Button.svelte";
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
    text-align: center;
    margin: 0 auto;
  }

  h1 {
    font-size: 2.8em;
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
  @media (min-width: 480px) {
    h1 {
      font-size: 4em;
    }
  }
</style>

<svelte:head>
  <title>Sapper project template</title>
  <script src="https://identity.netlify.com/v1/netlify-identity-widget.js">

  </script>
</svelte:head>

<h1>Make a Mask</h1>

<p>Find us on Facebook</p>
<p>
  Help keep our Healthcare workers safe in the Austin, Texas area. Personal
  Protective Equipment, especially masks are in dire need for their safety and
  can't be purchased through retailers.
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

<p>news blocks</p>
<p>news blocks</p>

<div id="faq">
  <h2>Frequently Asked Questions</h2>
  <p>etc</p>
</div>
