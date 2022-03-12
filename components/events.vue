<template>
  <div id="events" class="wrapper">
    <div class="event-header">
      <div class="background-header">МЕРОПРИЯТИЯ</div>
      <div class="inner-header">МЕРОПРИЯТИЯ</div>
    </div>
    <div class="events-container">
      <div class="items">
        <div class="item-1">
          <nuxt-link
            style="text-decoration: none; color: #fff45e"
            :to="`/events/schedule`"
          >
            Расписание мероприятий
          </nuxt-link>
        </div>
        <div class="item-2">
          <nuxt-link
            style="text-decoration: none; color: inherit"
            :to="`Events/schedule/archieve`"
          >
            Архив
          </nuxt-link>
        </div>
      </div>
      <div class="events">
        <div class="event-1">
          <div v-if="ip" class="date">
            <p class="date-1">
              {{ date }}
            </p>
            <p class="date-2">
              {{ ip[0].end_date }}
            </p>
          </div>
          <div v-if="ip" class="img-wrapper">
            <img :src="ip[0].main_photo" alt="" />
          </div>
          <div v-if="ip" class="title-speaker">
            <h2 class="title">
              {{ ip[0].title }}
            </h2>
            <p class="speaker">
              {{ ip[0].speaker }}
            </p>
          </div>
        </div>
        <div class="event-2">
          <div v-if="ip" class="date">
            <p class="date-1">
              {{ ip[1].start_date }}
            </p>
            <p class="date-2">
              {{ ip[1].end_date }}
            </p>
          </div>
          <div v-if="ip" class="img-wrapper">
            <img :src="ip[1].main_photo" alt="" />
          </div>
          <div v-if="ip" class="title-speaker">
            <h2 class="title">
              {{ ip[1].title }}
            </h2>
            <p class="speaker">
              {{ ip[1].speaker }}
            </p>
          </div>
        </div>
        <div class="event-3">
          <div v-if="ip" class="date">
            <p class="date-1">
              {{ ip[2].start_date }}
            </p>
            <p class="date-2">
              {{ ip[2].end_date }}
            </p>
          </div>
          <div v-if="ip" class="img-wrapper">
            <img :src="ip[2].main_photo" alt="" />
          </div>
          <div v-if="ip" class="title-speaker">
            <h2 class="title">
              {{ ip[2].title }}
            </h2>
            <p class="speaker">
              {{ ip[2].speaker }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      ip: '',
      date: ''
    }
  },
  methods: {
    async event() {
      const ip = await this.$axios.$get('https://smartpoint.me/api/event/')
      this.ip = ip

      const moment = require('moment')
      const d = new Date('2019/06/01')

      moment(d).format('MMMM d, YYYY') // June 1, 2019
      
      this.date = d
      // ip[0].start_date =  ip[0].start_date.moment().format("MMM Do YY")
      //  ip[0].start_date = new Date(year, month).toLocaleDateString("en-US")
    },
  },
  created() {
    return this.event()
  },
}
</script>
<style scoped>
@media (min-width: 1240px) {
  .events-container {
    width: 1200px;
    margin: 0 auto;
  }
}
@media (max-width: 760px) {
}
@media (max-width: 900px) {
  .background-header {
    font-size: 7rem !important;
  }
  .inner-header {
    font-size: 3rem !important;
    margin-top: -159px !important;
  }
  .events-container {
    width: 500px !important;
    margin: 0 auto !important;
  }
  .event-1,
  .event-2,
  .event-3 {
    display: block !important;
  }
}
@media (max-width: 1240px) {
  .events-container {
    width: 900px;
    margin: 0 auto;
  }
  .event-1,
  .event-2,
  .event-3 {
    margin-left: 0 !important;
  }
  .date {
    min-width: 136px !important;
    margin-right: 0 !important;
    margin-left: 0 !important;
  }
  .img-wrapper {
    min-width: 456px !important;
    margin-left: 25px !important;
    margin-right: 25px !important;
  }
}
.events {
  padding-top: 60px;
}
.event-1,
.event-2,
.event-3 {
  /* margin-left: 100px; */
  display: flex;
  padding-bottom: 50px;
}
.img-wrapper img {
  max-width: 100%;
}
.img-wrapper {
  align-items: center;
  min-width: 500px;
  text-align: center;
  margin-left: 50px;
  margin-right: 50px;
  max-height: auto;
  max-width: 488px;
}
.date {
  /* display: flex; */
  min-width: 200px;
  margin-right: 50px;
  margin-left: 50px;
}
.items {
  justify-content: right;
  display: flex;
  margin-right: 20px;
}
.title-speaker {
  margin-right: 50px;
}
.title {
  padding-bottom: 10px;
}
.item-1 a,
.item-2 a {
  margin-right: 20px;
  font-weight: 500;
  font-size: 15px;
  padding: 10px 35px 10px 35px;
  border-radius: 3px;
  text-decoration: none;
}
.item-2 a {
  margin-right: 20px;
  font-weight: 500;
  font-size: 15px;
  padding: 10px 35px 10px 35px;
  border-radius: 3px;
  text-decoration: none;
  color: #263164;
  border: 1px solid #263164;
}
.item-1 a {
  color: #fff45e;
  background-color: #263164;
  border: 1px solid #263164;
}
.wrapper {
  font-family: sans-serif;
  background-color: #fff;
  margin-bottom: 50px;
}
.inner-header {
  font-size: 6rem;
  color: #263164;
  left: 283px;
  font-weight: 600;
  top: -6px;
  text-align: center;
  padding-bottom: 80px;
  margin-top: -221px;
  padding-top: -24px;
}
.background-header {
  overflow: hidden;
  margin-top: 39px;
  font-size: 10rem;
  font-weight: 700;
  color: transparent;
  -webkit-text-stroke-width: 3px;
  -webkit-text-stroke-color: rgba(52, 52, 52, 0.05);
  margin-bottom: 66px;
}
</style>
