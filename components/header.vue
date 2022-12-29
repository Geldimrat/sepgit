<template>
  <div class="header">
    <div class="nav_menu">
      <div
        class="left"
        :style="`background: ${toggle_btn ? '#1e1e1e' : '#0c0c0c'}`"
      >
        <div class="logo_links">
          <div class="logo">
            <nuxt-link to="/"
              ><img
                src="~/static/sepgit_logo.svg"
                @click="toggle_btn_hide"
                alt=""
            /></nuxt-link>
          </div>
          <ul :class="[toggle_btn ? 'show_menu' : '', 'nav_links']">
            <li>
              <nuxt-link to="/#billboard"
                ><span @click="toggle_btn_hide">Billboard</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/#stories"
                ><span @click="toggle_btn_hide">Stories</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/#media"
                ><span @click="toggle_btn_hide">Media</span></nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/#partners"
                ><span @click="toggle_btn_hide">Partners</span></nuxt-link
              >
            </li>
            <div class="right">
              <div class="lang_dropdown">
                <button class="lang_btn">
                  <span>En</span><img src="~/static/lang_flags/en.svg" alt="" />
                </button>
                <div class="lang_content">
                  <button class="lang_btn">
                    <span>Tm</span
                    ><img src="~/static/lang_flags/tm.svg" alt="" />
                  </button>
                  <button class="lang_btn">
                    <span>Ru</span
                    ><img src="~/static/lang_flags/ru.svg" alt="" />
                  </button>
                </div>
              </div>
            </div>
          </ul>
        </div>
        <div :class="[toggle_btn ? 'hide_menu' : '', 'link_logo']">
          <nuxt-link to="/" class="web_logo">
            <img src="~/static/sanly_bilim_logo.svg" alt="" />
          </nuxt-link>
          <div
            :class="[toggle_btn ? 'hide_menu' : '', 'humburger_menu']"
            @click="toggle_btn_show"
          >
            <svg
              width="30"
              height="19"
              viewBox="0 0 30 19"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <rect width="30" height="3" rx="1.5" fill="#D9D9D9" />
              <rect x="5" y="8" width="25" height="3" rx="1.5" fill="#D9D9D9" />
              <rect
                x="15"
                y="16"
                width="15"
                height="3"
                rx="1.5"
                fill="#D9D9D9"
              />
            </svg>
          </div>
        </div>
        <div
          :class="[toggle_btn ? 'show_menu' : 'hide_menu']"
          @click="toggle_btn_hide"
          style="color: white"
        >
          X
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    const links = [
      {
        id: 1,
        href: '',
        name_tm: '',
        name_en: '',
        name_ru: '',
      },
    ]
    return {
      links,
      toggle_btn: false,
    }
  },
  methods: {
    toggle_btn_show() {
      this.toggle_btn = true
    },
    toggle_btn_hide() {
      this.toggle_btn = false
    },
  },
}
</script>

<style></style>
