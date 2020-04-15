<script>
const stories = [
{
  link: 'https://www.kxan.com/news/coronavirus/make-a-mask-providing-much-needed-mask-covers-to-austin-medical-workers/',
  imgsrc: 'kxan2.jpg',
  alt: 'Kxan Second Story'
 },
 {
  link: 'https://www.kvue.com/article/news/health/coronavirus/coronavirus-austin-homemade-masks-healthcare-workers/269-b1fbb5f5-06a8-4e6d-9ea1-dc837017bf61',
  imgsrc: 'kvue.jpg',
  alt: 'Kvue Story'
 }, 
 {
  link: 'https://telemundoaustin.com/news/local/grupo-de-austin-recluta-costureras-para-hacer-mscaras-para-profesionales-de-la-salud',
  imgsrc: 'telemundo.jpg',
  alt: 'Telemundo Story'
 }, 
 {
  link: 'https://communityimpact.com/austin/southwest-austin-dripping-springs/coronavirus/2020/03/27/dripping-springs-residents-pool-efforts-to-create-masks-for-the-austin-area-with-make-a-mask-austin/',
  imgsrc: 'communityImpact.jpg',
  alt: 'Community Impact Story'
 }, 
 {
  link: 'https://www.kxan.com/news/coronavirus/make-a-mask-heres-how-you-can-support-medical-professionals-from-home/',
  imgsrc: 'kxan.jpg',
  alt: 'Kxan Story'
 }, 
 {
  link: 'https://www.fashionablyaustin.com/austinites-sew-masks-for-local-healthcare-workers/',
  imgsrc: 'fashionablyAustin.jpg',
  alt: 'Fashionably Austin Story'
 }, 
]
</script>
<style  lang="scss">
.media {
 display:grid;
 grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
  grid-gap: 1em;
 grid-auto-flow: dense;
 grid-gap:15px;
 place-content: center;
 a {
  display:block;
 }
  img {
   width:100%;
   max-width: 100%;
   height:auto;
  }
}
 @media (max-width:  330px) {
  .media {
  grid-template-columns: repeat(auto-fill, minmax(250px, 250px));
 }
 }
</style>

<div class="media">
 {#each stories as story}
  <a rel="noreferrer" target="_blank" href="{story.link}">
    <img src="{story.imgsrc}" alt="{story.alt}">
  </a>
 {/each}
</div>