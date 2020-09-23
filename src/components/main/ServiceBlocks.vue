<template>
  <div class="flex mx-auto flex-col md:flex-row flex-wrap gap-2">
<!--    <div class="ml-auto  bg-gray-500 h-12" style="width: 590px"></div>-->
<!--    <div class="mr-auto  bg-gray-400 h-12" style="width: 474px"></div>-->
    <AppServiceCard big-block class="ml-auto" :background-image="blockOne">
      <t-button>
        test
<!--        <font-awesome-icon icon="arrow-right" />-->
        <i class="fas fa-arrow-right"></i>
      </t-button>
    </AppServiceCard>
    <AppServiceCard class="mr-auto" :background-image="blockTwo">

    </AppServiceCard>
  </div>
</template>m

<script>
import AppServiceCard from "../app/AppServiceCard";
export default {
name: "ServiceBlocks",
  components: {AppServiceCard},
  computed: {
    blockOne() {
      return require('../../../static/img/block3.jpg')
    },
    blockTwo() {
      return require('../../../static/img/block4.jpg')
    },
  }
}
</script>

<style scoped>

</style>