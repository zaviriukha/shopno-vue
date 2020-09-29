<template>
  <div class="lg:pt-40 sm:pt-20 pt-10 sm:pr-16 sm:pr-8 pr-4 pb-10 sm:pl-8 pl-4 bg-cover bg-no-repeat w-11/12" :class="[bigBlock?'bigBlock':'smallBlock']" :style="{ backgroundImage: `url('${backgroundImage}')`  }">
    <div class="text-lg pb-6 text-white font-bold uppercase ">{{ title}}</div>
    <div class="pb-16 text-base text-white">{{ shortDesc}}</div>
    <slot/>
  </div>
</template>

<script>
export default {
  name: "AppServiceCard",
  props: {
    bigBlock: Boolean,
    backgroundImage: String,
    title: String,
    prevText: String,
    shortDesc: String
  },
  computed: {
    // width: function () {
    //   return this.smallBlock ? 474 : 590
    // }
    // style() {
    //   return 'background-image: url(' + this.backgroundImage + ')';
    // }
  }
}
</script>

<style scoped lang="scss">
.bigBlock{
  width: 590px;
}

.smallBlock{
  width: 474px;
}

@media screen and (max-width: 736px) and (min-width: 540px) {
  .smallBlock {
    width: 510px;
  }
  .bigBlock{
    width: 510px;
  }
}

@media screen and (max-width: 414px){
  .smallBlock {
    width: 380px;
  }
  .bigBlock{
    width: 380px;
  }
}

@media screen and (max-width: 375px){
  .smallBlock {
    width: 340px;
  }
  .bigBlock{
    width: 340px;
  }
}


</style>