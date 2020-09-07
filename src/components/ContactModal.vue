<template>
  <div class="py-20">
    <button
        class="text-lg bg-transparent uppercase hover:bg-teal-1010 text-gray-1010 font-semibold  py-2 px-4 border border-gray-1020 hover:border-gray-1030 rounded"
        @click="$refs.modal.show()" type="button">Contact us
    </button>

    <t-modal ref="modal">
      <template v-slot:close>
        <a class="close-button" href="#">Close</a>
      </template>
      <template slot="header">
        CONTACT US
      </template>
      <div>
        gjfjfjfjfhfh
      </div>
      <template v-slot:footer>
        <div class="flex justify-center">
          <t-button type="button" @click="$refs.modal.hide()">
            Cancel
          </t-button>
        </div>
      </template>
    </t-modal>
  </div>
</template>

<script>

export default {
  name: "ContactModal",
  data() {
    return {
      showModal: false
    }
  }
}
</script>

<style lang="scss">
.close-button {
  width: 40px;
  height: 40px;
  box-shadow: 0 10px 10px 10px rgba(0, 0, 0, 0.25);
  border-radius: 10px;
  background: none;
  left: 50%;
  top: 50%;
  margin-top: -20px;
  margin-left: -20px;
  position: absolute;
  display: block;
  z-index: 200;
  text-indent: -9999px;
}

.close-button:before,
.close-button:after {
  content: '';
  width: 55%;
  height: 2px;
  background: #fff;
  position: absolute;
  top: 48%;
  left: 22%;
  -webkit-transform: rotate(-45deg);
  -moz-transform: rotate(-45deg);
  -ms-transform: rotate(-45deg);
  -o-transform: rotate(-45deg);
  transform: rotate(-45deg);
  -webkit-transition: all 0.3s ease-out;
  -moz-transition: all 0.3s ease-out;
  -ms-transition: all 0.3s ease-out;
  -o-transition: all 0.3s ease-out;
  transition: all 0.3s ease-out;
}

.close-button:after {
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
  transform: rotate(45deg);
  -webkit-transition: all 0.3s ease-out;
  -moz-transition: all 0.3s ease-out;
  -ms-transition: all 0.3s ease-out;
  -o-transition: all 0.3s ease-out;
  transition: all 0.3s ease-out;
}

.close-button:hover:before,
.close-button:hover:after {
  -webkit-transform: rotate(180deg);
  -moz-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  -o-transform: rotate(180deg);
  transform: rotate(180deg);
  background: #0787FA !important;
}
</style>