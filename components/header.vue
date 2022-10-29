<template>
  <div class="nav_menu">
    <div class="left">
      <div class="logo">
        <nuxt-link to="/"
          ><img src="~/static/sepgit_logo.svg" alt=""
        /></nuxt-link>
      </div>
      <ul class="nav_links">
        <li><nuxt-link to="#billboard">Billboard</nuxt-link></li>
        <li><nuxt-link to="#stories">Stories</nuxt-link></li>
        <li><nuxt-link to="#media">Media</nuxt-link></li>
        <li><nuxt-link to="#partners">Partners</nuxt-link></li>
      </ul>
      <div class="link_logo">
        <nuxt-link to="/">
          <img src="~/static/sanly_bilim_logo.svg" alt="" />
        </nuxt-link>
      </div>
    </div>
    <div class="right">
      <div class="lang_dropdown">
        <button class="lang_btn">
          <span>En</span><img src="~/static/lang_flags/en.svg" alt="" />
        </button>
        <div class="lang_content">
          <button class="lang_btn">
            <span>Tm</span><img src="~/static/lang_flags/tm.svg" alt="" />
          </button>
          <button class="lang_btn">
            <span>Ru</span><img src="~/static/lang_flags/ru.svg" alt="" />
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    const links = [
      {
        id: 1,
        href: '',
        name_tm: '',
        name_en: '',
        name_ru: '',
      }
    ]
    return{
      links
    }
  }
}
</script>

<style></style>
