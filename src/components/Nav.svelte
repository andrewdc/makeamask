<script>
  export let segment;
</script>

<style>

  nav {
    border-bottom: 1px solid rgba(35,10,1,0.29);
    font-weight: 400;
    padding: 0 1em;
      background:#f0f0f0;
      z-index:10000;
      position: relative;
  }

  ul {
    margin: 0;
    padding: 0;
    display:flex;
  }

  /* clearfix */
  ul::after {
    content: "";
    display: block;
    clear: both;
  }

  li {
    display: block;
    flex:1 0 auto;
  }

  [aria-current] {
    position: relative;
  }

  [aria-current]::after {
    position: absolute;
    content: "";
    width: calc(100% - 1em);
    height: 2px;
    background-color: rgb(2, 110, 172);
    display: block;
    bottom: -1px;
  }

  a {
    position: relative;
    display:flex;
    align-items:center;
    justify-content:center;
    flex-direction:column;
    text-decoration: none;
    padding: 1em 0.5em;
    color:rgb(2, 110, 172);
    text-align:center;
  }
  a:hover:after {
    position: absolute;
    content: "";
    width: calc(100% - 1em);
    height: 2px;
    background-color: rgb(2, 110, 172);
    display: block;
    bottom: -1px;
  }
  img {
    width:50px;
  }
  @media (max-width: 510px) {
    nav{
      padding:0 3px;
    }
    img {
      width:25px;
    }
    a {
      font-size:0.85em;
      padding: 0.5em 0.2em;
    }
  }
  .faq {
    display:none;
  }
  @media (max-width:510px){
  .creators, .request, .faq {
    position:fixed;
    bottom:0px;
    z-index: 100;
    background:#f0f0f0;
    width:33.33vw;
  }
  .creators {left:0}
  .request {left:33.33vw}
  .faq {
    display:block;
    left:66.66vw;
  }
  }
</style>

<nav>
  <ul>
    <li>
      <a aria-current={segment === undefined ? 'page' : undefined} href=".">
         <img src="/icons/019-cloth.svg" alt="stitched cloth"> Home
      </a>
    </li>
    <li class="creators">
      <a
        aria-current={segment === 'creators' ? 'page' : undefined}
        href="creators">
        <img src="/icons/006-fashion-1.svg" alt="sewing maching"> Make a Mask
      </a>
    </li>
    <li class="request">
      <a
        aria-current={segment === 'providers' ? 'page' : undefined}
        href="providers">
        <img src="/icons/021-mask.svg" alt="medical mask">Request Masks
      </a>
    </li>
    <li>
      <a aria-current={segment === 'media' ? 'page' : undefined} href="media">
        <img src="/icons/004-clothes-1.svg" alt="iron"> Contact Media
      </a>
    </li>
    <li>
      <a aria-current={segment === 'about' ? 'page' : undefined} href="about">
        <img src="/icons/013-button.svg" alt="buttons">About
      </a>
    </li>
    <li class="faq">
      <a aria-current={segment === 'faq' ? 'page' : undefined} href="/#faq">
        <img src="/icons/001-brooch.svg" alt="buttons">FAQ
      </a>
    </li>

    <!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
    <!-- <li><a rel=prefetch aria-current='{segment === "blog" ? "page" : undefined}' href='blog'>blog</a></li> -->
  </ul>
</nav>
