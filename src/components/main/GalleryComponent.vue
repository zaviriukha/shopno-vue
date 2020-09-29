<template>
  <div class="flex  lg:flex-row flex-wrap justify-center gap-3">
    <vue-gallery :images="images" :index="index" @close="index = null"></vue-gallery>
    <div
        class="image "
        v-for="(image, imageIndex) in images"
        :key="imageIndex"
        @click="index = imageIndex"
        :style="{ backgroundImage: 'url(' + image + ')', width: '330px', height: '300px' }"
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
        require('../../../static/img/1.jpg'),
        require('../../../static/img/2.jpg'),
        require('../../../static/img/3.jpg'),
        require('../../../static/img/4.jpg'),
        require('../../../static/img/5.jpg'),
        require('../../../static/img/6.jpg')
      ],
      index: null
    }
  },
}
</script>

<style scoped>
.image {
  /*float: left;*/
  /*display: flex;*/
  cursor: pointer;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  border: 1px solid #ebebeb;
  /*margin: 5px 5px 5px 5px;*/
}
</style>