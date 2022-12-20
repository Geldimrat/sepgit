<template>
  <modal
    :adaptive="true"
    :draggable="false"
    :scrollable="false"
    name="dialog"
    class="dialog_modal"
    style="background: rgba(23, 23, 23, 0.65); backdrop-filter: blur(10px)"
  >
    <div class="dialog_content">
      <div class="profile">
        <div class="avatar">
          <!-- <img
            :src="require(`./../assets/images/stories/${conv_info.img}`)"
            alt=""
          /> -->
          {{ conv_info.img }}
        </div>
        <div class="info">
          <p class="fullname">Merjen Saparmyradova</p>
          <p class="major">Launch Life</p>
        </div>
      </div>
      <div class="conversation">
        <p class="text">
          {{ conv_info.text }}
        </p>
      </div>
    </div>
  </modal>
</template>

<script>
import Vue from 'vue'

export default {
  name: 'DialogModal',
  props: {
    conv_info: Object,
  },
  components: {},
  //   methods: {
  //     show() {
  //       this.$modal.show('dialog')
  //     },
  //     hide() {
  //       this.$modal.hide('dialog')
  //     },
  //   },
}
</script>

<style>
.vm--modal {
  position: relative !important;
  top: 60px !important;
  display: flex !important;
  background: transparent !important;
  box-shadow: none !important;
  overflow: visible !important;
}
</style>
