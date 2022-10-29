<template>
  <div class="main">
    <div class="header">
      <Header />
    </div>
    <nuxt />
    <div class="footer">
      <Footer />
    </div>
  </div>
</template>

<script>
import Header from '@/components/header.vue'
import Footer from '@/components/footer.vue'
export default {
  component: {
    Header,
    Footer,
  },
}
</script>

<style lang="scss" scoped></style>
