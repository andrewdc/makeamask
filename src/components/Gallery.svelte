<script>
 import Image from 'svelte-image';
</script>

<style lang="scss">

.container {
   display: flex;
  margin-top: 50px;
}

.container:focus-within a,
.container:hover a {
  transform: translateX(-25%);
}
a {
   position: relative;
  display: block;
  flex: 1 1 0px;
  transition: transform 500ms;
}
a:focus ~ a,
a:hover ~ a {
  transform: translateX(25%);
}

.container a:focus,
.container a:hover {
  transform: scale(2.5);
  z-index: 1;
}

</style>

<div class="container">
 <!-- <a href="#1">
  <Image class="img" src="gallery/gallery1.jpg"></Image>
 </a> -->
 <a href="/about">
 <Image class="img" src="gallery/gallery2.jpg"></Image>
 </a>
 <a href="/about">
 <Image class="img" src="gallery/gallery3.jpg"></Image>
 </a>
 <a href="/about">
 <Image class="img" src="gallery/gallery4.jpg"></Image>
 </a>
 <a href="/about">
 <Image class="img" src="gallery/gallery5.jpg"></Image>
 </a>
 <!-- <a href="#6">
 <Image class="img" src="gallery/gallery6.jpg"></Image>
 </a>
 <a href="#7">
 <Image class="img" src="gallery/gallery7.jpg"></Image>
 </a> -->
 <!-- <a href="#8">
 <Image class="img" src="gallery/gallery8.jpg"></Image>
 </a> -->
 <a href="/about">
 <Image class="img" src="gallery/gallery9.jpg"></Image>
 </a>
 <!-- <a href="#10">
 <Image class="img" src="gallery/gallery10.jpg"></Image>
 </a> -->
 <a href="#11">
 <Image class="img" src="gallery/gallery11.jpg"></Image>
 </a>
 <a href="#12">
 <Image class="img" src="gallery/gallery12.jpg"></Image>
 </a>
 <!-- <a href="#13">
 <Image class="img" src="gallery/gallery13.jpg"></Image>
 </a> -->
 <a href="#14">
 <Image class="img" src="gallery/gallery14.jpg"></Image>
 </a>
 <!-- <a href="#15">
 <Image class="img" src="gallery/gallery15.jpg"></Image>
 </a> -->

</div>