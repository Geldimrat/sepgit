<template>
  <div class="show_all_stories">
    <div class="top_stories">
      <div class="content">
        <div class="info">
          <p class="title">Stories</p>
          <p class="desc">I would like to tell...</p>
        </div>
        <div class="img">
          <img src="~/assets/images/stories/show_all.png" alt="" />
        </div>
      </div>
      <div class="top_icons">
        <img src="~/static/icons/show_top_mask.svg" alt="" />
      </div>
    </div>

    <div class="people_stories">
      <Card
        v-for="(e, i) in people"
        :key="i"
        :single_card="e"
        @user_id="showID"
      />
    </div>
    <DialogModal :conv_info="user_info" />
  </div>
</template>

<script>
import Card from '@/components/show_all_card.vue'
import DialogModal from '@/components/dialog.vue'
export default {
  components: {
    Card,
    DialogModal,
  },
  data() {
    const people = [
      {
        id: 1,
        img: '1.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#282C50',
      },
      {
        id: 2,
        img: '2.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#6A48B1',
      },
      {
        id: 3,
        img: '3.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#1B8861',
      },
      {
        id: 4,
        img: '1.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#282C50',
      },
      {
        id: 5,
        img: '2.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#6A48B1',
      },
      {
        id: 6,
        img: '3.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#1B8861',
      },
      {
        id: 7,
        img: '1.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#282C50',
      },
      {
        id: 8,
        img: '2.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#6A48B1',
      },
      {
        id: 9,
        img: '3.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#1B8861',
      },
      {
        id: 10,
        img: '1.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#282C50',
      },
      {
        id: 11,
        img: '2.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#6A48B1',
      },
      {
        id: 12,
        img: '3.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#1B8861',
      },
      {
        id: 13,
        img: '1.png',
        text: 'I am Lyudmila. I am Quality Control Engineer in Industrial Construction. When I was younger, I heard many stories from grandfather who was a civil engineer. The stories inspired me to eventually become an engineer. My advice for woman..',
        back_color: '#282C50',
      },
    ]
    return {
      user_info: {},
      people,
    }
  },
  methods: {
    showID(id) {
      this.people.forEach((e) => {
        if (e.id == id) {
          this.user_info = e
        }
      })
    },
  },
}
</script>

<style></style>
