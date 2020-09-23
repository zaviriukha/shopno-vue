<template>
  <div class="container mx-auto mb-20" id="projects">
    <div class="w-full  text-center pb-16">
      <h2 class="text-3xl lg:text-45 font-bold">FEATURED WORKS</h2>
      <h3 class="text-18 uppercase pt-6 font-bold">Lorem ipsum dolor sit amet event landing template</h3>
    </div>
      <GalleryComponent/>
  </div>

</template>

<script>
import GalleryComponent from "./GalleryComponent";
export default {
  name: "GallerySection",
  components: {GalleryComponent}
}
</script>

<style scoped>

</style>