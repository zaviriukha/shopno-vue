<template>
  <Carousel>
    <slide>
      Slide 1 Content
    </slide>
    <Slide>
      Slide 2 Content
    </Slide>
  </Carousel>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';

export default {
  name: "AppSlider",
  components: {
    Carousel,
    Slide
  },
  data() {
    return {};
  },
}
</script>

<style scoped>

</style>