<template>
  <vueper-slides fade :touchable="false" autoplay :arrows="false" fixed-height="450px">
    <vueper-slide
        v-for="(slide, i) in slides"
        :key="i"
        :image="slide.image"
        :title="slide.title"
        :content="slide.content"/>
  </vueper-slides>
</template>

<script>
import {VueperSlides, VueperSlide} from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'

export default {
  name: "AboutSlider",
  components: {VueperSlides, VueperSlide},
  data() {
    return {
      slides: [
        {
          title: 'El Teide Volcano, Spain',
          content: 'Photo by Max Rive',
          image: require('../../static/img/m1.jpg')
        },
        {
          title: 'El Teide Volcano, Spain',
          content: 'Photo by Max Rive',
          image: require('../../static/img/m2.jpg')
        },
        {
          title: 'El Teide Volcano, Spain',
          content: 'Photo by Max Rive',
          image: require('../../static/img/m3.jpg')
        },
        {
          title: 'El Teide Volcano, Spain',
          content: 'Photo by Max Rive',
          image: require('../../static/img/m4.jpg')
        },
      ]
    };
  },
}
</script>

<style scoped>

</style>