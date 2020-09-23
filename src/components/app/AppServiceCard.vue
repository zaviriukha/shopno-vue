<template>
  <div class="pt-40 pr-16 pb-10 pl-8  w-11/12" :class="[bigBlock?'bigBlock':'smallBlock']" :style="{ backgroundImage: `url('${backgroundImage}')`  }">
    <div class="text-lg pb-6 text-white font-bold uppercase ">Designing is The Cool</div>
    <div class="pb-16 text-base text-white">Our most popular service is our Virtual Receptionist. We know that ...</div>
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
    prevText: String
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

<style scoped>
.bigBlock{
  width: 590px;
}
.smallBlock{
  width: 474px;
}
</style>