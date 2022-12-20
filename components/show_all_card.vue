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
      <button class="read_more" @click="id(single_card.id)">read more</button>
      <div class="bottom_right"></div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    single_card: Object,
  },
  methods: {
    id(e) {
      this.$emit('user_id', e)
      this.$modal.show('dialog')
    },
  },
}
</script>

<style></style>
