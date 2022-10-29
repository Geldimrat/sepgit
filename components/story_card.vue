<template>
  <div class="story_card" :style="`background: ${card_info.back_color}`">
    <div class="content">
      <p class="info">
        {{ card_info.text }}
      </p>
      <nuxt-link to="" class="read_more">read more</nuxt-link>
      <div class="bottom_right"></div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    card_info: Object,
  },
}
</script>

<style></style>
