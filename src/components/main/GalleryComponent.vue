<template>
  <div>
    <vue-gallery :images="images" :index="index" @close="index = null"></vue-gallery>
    <div
        class="image"
        v-for="(image, imageIndex) in images"
        :key="imageIndex"
        @click="index = imageIndex"
        :style="{ backgroundImage: 'url(' + image + ')', width: '300px', height: '200px' }"
    ></div>
  </div>
</template>

<script>
import VueGallery from 'vue-gallery';

export default {
  name: "GalleryComponent",
  components: {VueGallery},
  data: function () {
    return {
      images: [
        require('../../../static/img/m1.jpg'),
        require('../../../static/img/m2.jpg'),
        require('../../../static/img/m3.jpg'),
        require('../../../static/img/m4.jpg')
      ],
      index: null
    }
  },
}
</script>

<style scoped>
.image {
  float: left;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  border: 1px solid #ebebeb;
  margin: 5px 5px 48px 5px;
}
</style>