<script>
  import ContactCard from "../components/ContactCard.svelte";
  import Button from "../components/Button.svelte";
  import SuperLink from "../components/SuperLink.svelte";
  import Faq from "../components/Faq.svelte";
</script>

<style>
.contacts {
  display:flex;
  flex-wrap:wrap;
  margin:20px 0;
}
:global(h3) {
font-size:1.6em;
font-weight:400;
padding: 0.6em 0 0.6em 0;
margin: 0 0 1em 0;
}

:global(h4) {
font-size:1.5em;
border-bottom:1px solid #55b9f3;
padding: 0 0 0.2em 0;
margin: 0 0 1em 0;
}

ol {
  list-style: none;
  counter-reset: my-awesome-counter;
  display: flex;
  flex-wrap: wrap;
  margin: 0;
  padding: 0;
}
ol li {
  counter-increment: my-awesome-counter;
  display: flex;
  width: 100%;
  /* font-size: 0.8rem; */
  margin-bottom: 2rem;
}
ol li::before {
  content: "0" counter(my-awesome-counter);
  font-weight: bold;
  font-size: 3rem;
  margin-right: 0.5rem;
  font-family: 'alegreya', serif;
  line-height: 1;
}
  .learn {
    display:flex;
    flex-direction:column;
    /* align-items:center; */
  }
  .learn img {
    width:50px;
  }
  .vids {
    display:flex;
    justify-content: center;
    /* align-items:center; */
    flex-direction:column;
  }

  .embed-container {margin-bottom:2em; position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }
</style>

<svelte:head>
  <title>Mask Creators - Make A Mask</title>
</svelte:head>

<h2>How can I help create Masks?</h2>

<h3 id="#learn" class="learn"><img src="/icons/011-design.svg" alt="sewing template"> Sewing Tutorials</h3>
<div class="vids">

<style></style><div class='embed-container'><iframe title='Learn to Sew a Mask Video' src='https://www.facebook.com/plugins/video.php?href=https%3A%2F%2Fwww.facebook.com%2Fmark.lewis.127%2Fvideos%2F3447045531977409%2F&show_text=1' style='border:none;overflow:hidden' scrolling='no' frameborder='0' allowTransparency='true' allow='encrypted-media' allowFullScreen='true'></iframe></div>


<div class='embed-container'><iframe title='Deaconess Health Mask Tutorial' width='560' height='315' src='https://www.youtube.com/embed/9tBg0Os5FWQ' frameborder='0' allow='accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture' allowfullscreen></iframe></div>
<!-- <iframe title="Learn to Sew a Mask Video" src="https://www.facebook.com/plugins/video.php?href=https%3A%2F%2Fwww.facebook.com%2Fmark.lewis.127%2Fvideos%2F3447045531977409%2F&show_text=1&width=560" width="560" height="514" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowTransparency="true" allow="encrypted-media" allowFullScreen="true"></iframe> -->
<!-- <iframe title="Deaconess Health Mask Tutorial" width="560" height="315" src="https://www.youtube.com/embed/9tBg0Os5FWQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->


</div>
<ul>

<li>
<SuperLink href="https://drive.google.com/file/d/1Gnmp7qOThe0jHu9us4_clfIKGAv-fBML/view?usp=sharing">Click to download pdf on how to sew an N95 cover</SuperLink>
</li>
<li>
<SuperLink href="https://www.facebook.com/mark.lewis.127/videos/3447045531977409/">Click to see tutorial on how to sew a surgical mask cover</SuperLink>
</li>
</ul>





<h3>
  I HAVE AN IDEA OF HOW MANY MASKS I AM GOING TO MAKE, OR HAVE COMPLETED MAKING
  THEM….HOW CAN I GET THE COMPLETED MASKS TO HEALTHCARE WORKERS IN AUSTIN?
</h3>
<ol>
  <li>
  <div>
    <h4>Volunteers Log your Make-A-Mask Contribution</h4>

    <p>
      The reason it is important to log your masks is it will allow us to start
      the planning process as to where to allocate them.
    </p>
    <p>
      IF POSSIBLE: PLEASE SEND A FEW GALLON SIZE ZIPLOCK BAGS WITH THE MASKS AS
      WE ARE TRYING TO PACKAGE THESE IN SETS OF 25 TO DISPERSE OUT.
    </p>
    <p>
      ALSO, INCLUDE A NOTE IF THEY HAVE BEEN LAUNDERED “AFTER” THE SEWING
      PROCESS SO WE CAN EXPEDITE GETTING THEM OUT.
    </p>
<Button newtab="true" href="https://forms.gle/CrjJDwR6KbVhyLHC9">
    <img slot="icon" src="/icons/005-dressmaker.svg" style="width:50px;" alt="measuring tape" />
    <span slot="text">  Log Your Contribution</span>
</Button>
    <!-- <a class="soft" href="https://forms.gle/CrjJDwR6KbVhyLHC9">
    </a> -->
    </div>
  </li>
  <li>
  <div>
    <h4>Choose a shipping location:</h4>

    <p>We now have a second location that is SHIP TO ONLY. I do not want people dropping off at one of my clinics because we are actively seeing both healthy and walk-in "sick" patients that go through a strict screening process. </p>
    <div class="contacts">
    <ContactCard>
      <span slot="instruction">
        SHIP TO or PORCH DROP OFF:
      </span>
      
      <span slot="name">
        Jennifer Reyes
      </span>
      <span slot="address">
      163 Open Sky Road<br>
Austin, TX 78737
      </span>
    </ContactCard>
        <ContactCard>
      <span slot="instruction">
        SHIP TO ONLY:
      </span>
      
      <span slot="name">
        Victory Medical <br>
        <em>c/o Jennifer Reyes - MASKS</em>
      </span>
      <span slot="address">
      4303 Victory Drive<br>
Austin, Texas 78704
      </span>
    </ContactCard>
</div>
    <p>We are creating teams to disperse the masks to clinics in the surrounding areas. I routinely network with other Directors and Practice Administrators in the Austin area and have direct contacts to share the masks with.</p>
    </div>
  </li>
</ol>

<Faq></Faq>