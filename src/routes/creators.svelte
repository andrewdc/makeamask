<script>
  import ContactCard from "../components/ContactCard.svelte";
  import Button from "../components/Button.svelte";
  import SuperLink from "../components/SuperLink.svelte";
  import Faq from "../components/Faq.svelte";
  import Image from "svelte-image";
</script>

<style>
  .contacts {
    display: flex;
    flex-wrap: wrap;
    margin: 20px 0;
  }
  :global(h3) {
    font-size: 1.6em;
    font-weight: 400;
    padding: 0.6em 0 0.6em 0;
    margin: 0 0 1em 0;
  }

  :global(h4) {
    font-size: 1.5em;
    border-bottom: 1px solid #55b9f3;
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
    font-family: "alegreya", serif;
    line-height: 1;
  }
  .learn {
    display: flex;
    flex-direction: column;
    /* align-items:center; */
  }
  .learn img {
    width: 50px;
  }
  .vids {
    display: flex;
    justify-content: center;
    /* align-items:center; */
    flex-direction: column;
  }
  .embed-container {
    margin-bottom: 2em;
    position: relative;
    padding-bottom: 56.25%;
    height: 0;
    overflow: hidden;
    max-width: 100%;
  }
  .embed-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
  dt {
    font-weight: bold;
  }
</style>

<svelte:head>
  <title>Mask Creators - Make A Mask</title>
  <meta
    name="Description"
    content="How do I sew a mask? Learn here with tutorials and mask patterns" />
</svelte:head>

<h2>How can I help create Masks?</h2>

<h3 id="#learn" class="learn">
  <img src="/icons/011-design.svg" alt="sewing template" />
  Mask Cover Step-by-Step Tutorial
</h3>

<ul>
  <li>
    <SuperLink href="/Mask-Covers_Step-By-Step_Instructions.pdf">
      Mask Covers Instructions PDF
    </SuperLink>
  </li>
  <li>
    <SuperLink href="/Mask-Covers_Step-By-Step_Instructions.docx">
      Mask Covers Instructions docx
    </SuperLink>
  </li>
</ul>
<div class="vids">

  <ol>
    <li>
      <p>
        Cut ONE piece of fabric at 10.5 inches by 7.5 inches and then TWO
        smaller pieces at 7.5 inches by 5.5 inches.
        <br />
        <Image src="/howto/IMG_9161.jpg" alt="paper template" />
      </p>
    </li>
    <li>
      <p>
        Take the smaller pieces, turn them facedown and fold the boDom up approximately 3/4 inch. Stitch that. Do the same for the other smaller piece.
        <br />
        <Image src="/howto/IMG_9162.jpg" alt="paper template" />
        <Image src="/howto/IMG_9163.jpg" alt="paper template" />
        <Image src="/howto/IMG_9164.jpg" alt="paper template" />
      </p>
    </li>
    <li>
      <p>
        Take the larger piece, lay it face up, and place one of the smaller pieces centered on the main piece along the top. The smaller piece should be facedown. The sewn (hem) part should be toward the middle of the larger fabric.
Do this for both smaller pieces (one at top and one at bottom).
        <br />
        <Image src="/howto/IMG_9165.jpg" alt="paper template" />
        <Image src="/howto/IMG_9166.jpg" alt="paper template" />
        <Image src="/howto/IMG_9167.jpg" alt="paper template" />
      </p>
    </li>
    <li>
      <p>
        After sewing both the smaller pieces to the larger piece.
Turn the smaller pieces out, so that they are extended out from the larger piece, and iron them flat.
        <br />
        <Image src="/howto/IMG_9168.jpg" alt="paper template" />
      </p>
    </li>
    <li>
      <p>
        Flip the larger piece facedown and then fold the smaller pieces back on top, so they are facing down toward the middle of the larger piece again. Iron flat.
        <br />
        <Image src="/howto/IMG_9169.jpg" alt="paper template" />
      </p>
    </li>
    <li>
      <p>
        Holding it all together, flip it back over again so that the smaller pieces are under the larger piece and then you will accordion it two times to make the “folds” in the fabric. Each Hme making sure to get both the top and bottom pieces.
        <br />
        <Image src="/howto/IMG_9170.jpg" alt="paper template" />
      </p>
    </li>
    <li>
      <p>
        Pin each fold as you go and then sew the edges approximately 1 inch from the end.
        <br />
        <Image src="/howto/IMG_9171.jpg" alt="paper template" />
        <Image src="/howto/IMG_9172.jpg" alt="paper template" />
        <Image src="/howto/IMG_9173.jpg" alt="paper template" />
      </p>
    </li>
    <li>
      <p>
        Cut 1/4 inch elastic approximately 10 inches long. Secure the ends together overlapping approximately 1 inch to make a circle with the elastic. Fold each end of the mask cover over approximately 1 inch from the end (about where you have previously stitched). Place one elasHc circle, or an XL elastic hair tie, in the folded piece of the end, and then fold under just a little of the end to make a hem. Sew this down. It should be approximately 3/4 of an inch from the end of the fabric. Do this for both ends.
        <br />
        <Image src="/howto/IMG_9174.jpg" alt="paper template" />
        <Image src="/howto/IMG_9175.jpg" alt="paper template" />
        <Image src="/howto/IMG_9176.jpg" alt="paper template" />
        <Image src="/howto/IMG_9177.jpg" alt="paper template" />
        <Image src="/howto/IMG_9178.jpg" alt="paper template" />
      </p>
    </li>
  </ol>
  <!-- <div class="embed-container">
    <iframe
      title="Learn to Sew a Mask Video"
      src="https://www.facebook.com/plugins/video.php?href=https%3A%2F%2Fwww.facebook.com%2Fmark.lewis.127%2Fvideos%2F3447045531977409%2F&show_text=1"
      style="border:none;overflow:hidden"
      scrolling="no"
      frameborder="0"
      allowTransparency="true"
      allow="encrypted-media"
      allowFullScreen="true" />
  </div>

  <div class="embed-container">
    <iframe
      title="Deaconess Health Mask Tutorial"
      width="560"
      height="315"
      src="https://www.youtube.com/embed/9tBg0Os5FWQ"
      frameborder="0"
      allow="accelerometer; autoplay; encrypted-media; gyroscope;
      picture-in-picture"
      allowfullscreen />
  </div> -->

</div>

<h3>
  I HAVE AN IDEA OF HOW MANY MASKS I AM GOING TO MAKE, OR HAVE COMPLETED MAKING
  THEM….HOW CAN I GET THE COMPLETED MASKS TO HEALTHCARE WORKERS IN AUSTIN?
</h3>
<ol>
  <li>
    <div>
      <h4>Volunteers Log your Make-A-Mask Contribution</h4>

      <p>
        The reason it is important to log your masks is it will allow us to
        start the planning process as to where to allocate them.
      </p>
      <p>
        IF POSSIBLE: PLEASE SEND A FEW GALLON SIZE ZIPLOCK BAGS WITH THE MASKS
        AS WE ARE TRYING TO PACKAGE THESE IN SETS OF 20 TO DISPERSE OUT.
      </p>
      <p>
        ALSO, INCLUDE A NOTE IF THEY HAVE BEEN LAUNDERED “AFTER” THE SEWING
        PROCESS SO WE CAN EXPEDITE GETTING THEM OUT.
      </p>
      <Button
        error="true"
        newtab="true"
        href="https://forms.gle/CrjJDwR6KbVhyLHC9">
        <img
          slot="icon"
          src="/icons/005-dressmaker.svg"
          style="width:50px;"
          alt="measuring tape" />
        <span slot="text">Log Your Contribution</span>
      </Button>
      <!-- <a class="soft" href="https://forms.gle/CrjJDwR6KbVhyLHC9">
    </a> -->
    </div>
  </li>
  <li>
    <div>
      <h4>Choose a shipping location:</h4>

      <p>
        We now have a second location that is SHIP TO ONLY. I do not want people
        dropping off at one of my clinics because we are actively seeing both
        healthy and walk-in "sick" patients that go through a strict screening
        process.
      </p>
      <div class="contacts">
        <ContactCard>
          <span slot="instruction">SHIP TO or PORCH DROP OFF:</span>

          <span slot="name">Jennifer Reyes</span>
          <span slot="address">
            163 Open Sky Road
            <br />
            Austin, TX 78737
          </span>
        </ContactCard>
        <ContactCard>
          <span slot="instruction">SHIP TO ONLY:</span>

          <span slot="name">
            Victory Medical
            <br />
            <em>c/o Jennifer Reyes - MASKS</em>
          </span>
          <span slot="address">
            4303 Victory Drive
            <br />
            Austin, Texas 78704
          </span>
        </ContactCard>
      </div>
      <p>
        We are creating teams to disperse the masks to clinics in the
        surrounding areas. I routinely network with other Directors and Practice
        Administrators in the Austin area and have direct contacts to share the
        masks with.
      </p>
    </div>

    <!-- <iframe src="https://www.google.com/maps/d/embed?mid=1MPnTVNWY959yFKxns-1Gok0lcc2r4Aa2" width="640" height="480"></iframe> -->

  </li>
</ol>
<h4 id="dropOff">Drop off locations:</h4>
<div class="embed-container">
  <iframe
    title="drop off locations map"
    src="https://www.google.com/maps/d/embed?mid=1MPnTVNWY959yFKxns-1Gok0lcc2r4Aa2"
    width="640"
    height="480" />
</div>
<dl>
  <dt>Honey Bee Quilt Store</dt>
  <dd>
    All DROPS here by 3pm, please. Collection bin right outside the door. Ffyi:
    Honey Bee is open for online/phone orders and curbside pick-up. Thank you,
    Honey Bee! ;-)
    <br />
    <address>9308 Anderson Mill Rd, Austin, TX 78729</address>

  </dd>
  <dt>Tomlinson's Feed</dt>
  <dd>
    They open at 10am every day. ALL DROPS by 3pm, please. Collection bin right
    outside the door. Tomlinson's is open and wants to remain mindful about the
    traffic in their store, so please be respectful of their generosity.
    <br />
    <address>4211 S Lamar Blvd Ste A23, Austin, TX 78704</address>
  </dd>
  <dt>Mask Cover DROP - Personal Residence</dt>
  <dd>
    ALL DROPS here by 9pm, please. Please be mindful that this is a private
    residence. These will be safe / no contact porch drops. Thank you!
    <br />
    <address>163 Open Sky Rd, Austin, TX 78737</address>
  </dd>
</dl>

<Faq />
