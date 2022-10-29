<template>
  <div class="show_all_card" :style="`background: ${single_card.back_color}`">
    <div class="avatar">
      <img
        :src="require(`~/assets/images/stories/${single_card.img}`)"
        alt=""
      />
    </div>
    <div class="content">
      <p class="info">
        {{ single_card.text }}
      </p>
      <nuxt-link to="" class="read_more">read more</nuxt-link>
      <div class="bottom_right"></div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    single_card: Object,
  },
}
</script>

<style></style>
