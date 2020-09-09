<template>
  <div class="container mx-auto mb-20">
    <div class="w-full  text-center pb-16">
      <h2 class="text-3xl lg:text-45 font-bold">ABOUT US</h2>
      <h3 class="text-18 uppercase pt-6 font-bold">Lorem ipsum dolor sit amet event landing template</h3>
    </div>

    <div class=" flex flex-col md:flex-row flex-wrap gap-6">
      <div class="lg:w-1/3 w-full ml-auto ">
        <h4 class="text-xl pb-2">We Actually Do amazing works</h4>
        <p class="text-base pb-2">A visual approach is an approach to a runway at an airport conducted under instrument flight rules. The pilot must at all times have either the airport or the preceding aircraft in approach correct sight. Conducted under instrument flight rules. The pilot must at all times.</p>
        <p class="text-base pb-2">Preceding aircraft in approach correct sight. conducted under instrument flight rules.</p>
        <h4 class="text-xl pb-2">Why we are the great?</h4>
        <p class="text-base pb-2">A visual approach is an approach to a runway at an airport conducted under instrument flight rules. The preceding aircraft in approach correct sight.</p>
      </div>
      <div class="lg:w-1/3 w-full mr-auto ">
        <AboutSlider/>
      </div>
    </div>

  </div>
</template>

<script>
import AboutSlider from "../AboutSlider";
export default {
name: "AboutSection",
  components: {AboutSlider}
}
</script>

<style scoped>

</style>