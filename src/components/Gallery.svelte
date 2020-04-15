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
  transform: scale(1.5);
  z-index: 1;
}

</style>

<div class="container">
 <a href="#1">
  <Image class="img" src="gallery/gallery1.jpg"></Image>
 </a>
 <a href="#2">
 <Image class="img" src="gallery/gallery2.jpg"></Image>
 </a>
 <a href="#3">
 <Image class="img" src="gallery/gallery3.jpg"></Image>
 </a>
 <a href="#4">
 <Image class="img" src="gallery/gallery4.jpg"></Image>
 </a>
 <a href="#5">
 <Image class="img" src="gallery/gallery5.jpg"></Image>
 </a>
 <a href="#6">
 <Image class="img" src="gallery/gallery6.jpg"></Image>
 </a>
 <a href="#7">
 <Image class="img" src="gallery/gallery7.jpg"></Image>
 </a>

</div>