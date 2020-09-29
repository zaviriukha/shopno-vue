<template>
  <div>
    <div class="flex  flex-col md:flex-row flex-wrap gap-2">
      <AppServiceCard big-block class="lg:ml-auto mx-auto lg:mx-0" :background-image="blockOne"
                      short-desc="Our most popular service is our Virtual Receptionist. We know that ..."
                      title="Designing is The Cool">
        <t-button>
          test
        </t-button>
      </AppServiceCard>
      <AppServiceCard class="lg:mr-auto mx-auto lg:mx-0" :background-image="blockTwo"
                      title="cool psd Design"
                      short-desc="Our most popular service is our we know that sometimes it’s ..">
        <t-button>
          test
        </t-button>
      </AppServiceCard>
    </div>

    <div class="flex mt-2 flex-col md:flex-row flex-wrap gap-2">
      <AppServiceCard big-block class="lg:ml-auto mx-auto lg:mx-0" :background-image="blockTree"
                      short-desc="Our most popular service is our Virtual Receptionist. We know that ..."
                      title="Designing is The Cool">
        <t-button>
          test
        </t-button>
      </AppServiceCard>
      <AppServiceCard class="lg:mr-auto mx-auto lg:mx-0" :background-image="blockFour"
                      title="cool psd Design"
                      short-desc="Our most popular service is our we know that sometimes it’s ..">
        <t-button>
          test
        </t-button>
      </AppServiceCard>
    </div>

    <div class="flex mt-2 flex-col md:flex-row flex-wrap gap-2">
      <AppServiceCard  class="lg:ml-auto mx-auto lg:mx-0" :background-image="blockFive"
                      short-desc="Our most popular service is our Virtual Receptionist. We know that ..."
                      title="Designing is The Cool">
        <t-button>
          test
        </t-button>
      </AppServiceCard>
      <AppServiceCard big-block class="lg:mr-auto mx-auto lg:mx-0" :background-image="blockSix"
                      title="cool psd Design"
                      short-desc="Our most popular service is our we know that sometimes it’s ..">
        <t-button>
          test
        </t-button>
      </AppServiceCard>
    </div>
  </div>

</template>

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
    blockTree() {
      return require('../../../static/img/block.jpg')
    },
    blockFour() {
      return require('../../../static/img/block2.jpg')
    },
    blockFive() {
      return require('../../../static/img/block5.jpg')
    },
    blockSix() {
      return require('../../../static/img/block6.jpg')
    },
  }
}
</script>

<style scoped>

</style>