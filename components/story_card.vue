<template>
  <div class="story_card" :style="`background: ${card_info.back_color}`">
    <div class="content">
      <p class="info">
        {{ card_info.text }}
      </p>
      <button to="" class="read_more" @click="id(card_info.id)">
        read more
      </button>
      <div class="bottom_right"></div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    card_info: Object,
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
