<template>
  <div class="container mx-auto mb-20" id="service">
    <div class="w-full  text-center pb-16">
      <h2 class="text-3xl lg:text-45 font-bold">OUR SERVICES</h2>
      <h3 class="text-18 uppercase pt-6 font-bold">Lorem ipsum dolor sit amet event landing template</h3>
    </div>

  <ServiceBlocks/>

  </div>
</template>

<script>
import ServiceBlocks from "./ServiceBlocks";
export default {
name: "ServiceSection",
  components: {ServiceBlocks}
}
</script>

<style scoped>

</style>