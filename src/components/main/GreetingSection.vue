<template>
  <div class="hero container mx-auto flex flex-col sm:flex-row justify-between py-20">
    <div class="w-full  text-center ">
      <div class="text-3xl lg:text-45 font-bold">SAY HELLO TO <span class="bg-teal-1010 px-3">SHOPNO!</span></div>
      <div class="text-3xl lg:text-45 font-bold">AGENCY CORPORATE SHOPNO THEME</div>

      <ContactModal/>
    </div>
  </div> <!-- end hero -->
</template>

<script>
import ContactModal from "../ContactModal";
export default {
name: "GreetingSection",
  components: {ContactModal}
}
</script>

<style scoped>

</style>