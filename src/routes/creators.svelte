<script>
  import ContactCard from "../components/ContactCard.svelte";
</script>
<style>
.contacts {
  display:flex;
  margin:20px 0;
}
:global(h4) {
font-size:1.5em;
border-bottom:1px solid red;
padding: 0 0 0.2em 0;
margin: 0 0 1em 0;
}
@import url('https://fonts.googleapis.com/css?family=Abril+Fatface');

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
  font-family: 'Abril Fatface', serif;
  line-height: 1;
}

</style>
<svelte:head>
  <title>Mask Creators</title>
</svelte:head>

<h2>How can I help create Masks?</h2>

<h3 id="#learn">Sewing Tutorials</h3>
<a
  href="https://www.facebook.com/stephanie.angle/posts/10107637284178223?__tn__=K-R">
  Learn to sew an N95 cover
</a>
<a
  href="https://drive.google.com/file/d/1Gnmp7qOThe0jHu9us4_clfIKGAv-fBML/view?usp=sharing">
  Click to download pdf on how to sew an N95 cover
</a>
<a href="https://www.facebook.com/mark.lewis.127/videos/3447045531977409/">
  Click to see tutorial on how to sew a surgical mask cover
</a>

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

    <a href="https://forms.gle/CrjJDwR6KbVhyLHC9">Log Your Contribution</a>
    </div>
  </li>
  <li>
  <div>
    <h4>Choose a shipping location:</h4>

    <p>We now have a second location that is SHIP TO ONLY. I do not want people dropping off at one of my clinics because we are actively seeing both healthy and walkin "sick" patients that go through a strict screening process. </p>
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
    <p>Teams are being created now to see that they are dispersed to clinics in the surrounding areas.  I routinely network with other Directors and Practice Administrators in the Austin area and have direct contacts to share the masks with.</p>
    </div>
  </li>
</ol>

<h2>Frequently Asked Questions</h2>

<h3>WHERE ARE THE MASKS BEING DISTRIBUTED?</h3>
<p>
  Make-A-Mask was started in Austin, Texas by Jennifer Reyes, the Director of
  Clinical Operations, for the Victory Medical Urgent Care and Family Practice
  clinics. She reached out online as a desperate plea to get help from her local
  community in sewing masks and help solve her lack of PPE for her employees.
  Through the power of social media and a viral facebook page, there are
  thousands of people across the USA that have joined forces to drop off and/or
  ship sewn masks to the Austin area to help healthcare workers.
</p>

<h3>
  I’VE HEARD THAT FABRIC MASKS WON’T WORK OR HARBOR GERMS. HOW WILL THIS HELP
  MEDICAL STAFF?
</h3>
<p>
  Jennifer is a Director of Clinical Operations for family practice and urgent
  care clinics in the Austin area and personally struggles with having supplies
  for her own staff. It is advised that medical staff NEVER wear these as
  primary masks or only as a last resort. Our goal and instructions will be to
  share with clinics receiving masks on how to utilize the masks correctly and
  wear the sewn mask OVER the surgical or N95 mask. Kind of like a cover if you
  will. We can switch out the sewn mask in between each patient and prolong the
  life of our medical mask for a much longer period of time. Then, with the sewn
  masks, we can soak...launder... and repeat. That’s why we need mass quantities
  of sewn masks. Lots of patients = Lots of masks. We are working in unexplored
  territory at this time, and some protection is better than NO protection.
  These clinics WILL RUN OUT of all standard issued PPE soon.
</p>
<h3>WHAT IS THE BEST TYPE OF MATERIAL TO MAKE THE MASK OUT OF?</h3>
<p>
  Currently, we encourage you to use 100% cotton to make the masks. The medical
  staff will be wearing 2 masks (as stated above), so we want to make sure it’s
  something that is still comfortable and breathable. Some #MakeAMaskSewers have
  gotten creative with cotton, flannel, cloth diapers, T-shirts, pillowcases,
  etc. Be conscious about any additional “elements” you add to the masks. There
  are lots of patterns out there. The masks will need to be easily washed. In
  addition - the elastic is better than tie straps. Elastic is hard to come by
  right now, so we have seen #MakeAMaskSewers using elastic hair ties as a
  secondary option. We’ve heard about pipe cleaners being used to mold the
  bridge of the nose, and while genius, would make it difficult for laundering
  over and over.
</p>

<h3>
  I HAVE SEEN LOTS OF DIFFERENT TYPES OF MASKS...HOW DO I KNOW WHICH ONE TO MAKE
  ... BIGGER or SMALLER?
</h3>
<p>
  The bigger sewn masks that you have seen are meant to go over the N95 masks.
  The smaller sewn masks are meant to go over the surgical masks. To be honest,
  we need BOTH. Unfortunately, most of the clinics don’t normally stock large
  quantities of the N95 masks on a regular basis, so when it was time to quick
  order some… there were none to be found.. Therefore, most clinics are wearing
  surgical masks at this point. Bigger hospitals, when available, will be
  wearing more of the N95 masks. With that said, the government has made
  promises that more N95 masks are coming - SOMETIME. Our priority now is to
  supply the clinics, especially urgent care facilities, as that is where a
  majority of the walkin patients will be going for screening and testing.
</p>
