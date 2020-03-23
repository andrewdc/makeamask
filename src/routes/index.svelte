<script>
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
<em>...to become large button/links</em>
<a href="providers">Healthcare Providers</a>
|
<a href="creators">Mask Creators</a>

<h2>In the News</h2>

<p>news blocks</p>
<p>news blocks</p>

<div id="faq">
  <h2>Frequently Asked Questions</h2>
  <p>etc</p>
</div>
