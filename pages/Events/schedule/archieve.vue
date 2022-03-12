<template>
  <div class="wrapper">
    <div class="nav">
      <div class="nav-main">
        <nuxt-link
          style="text-decoration: none; color: inherit; cursor: pointer"
          :to="`/`"
        >
          Главная
        </nuxt-link>
      </div>
      <p style="padding-left: 5px; padding-right: 5px" class="space">></p>
      <div style="cursor: pointer" class="nav-schedule">Архив</div>
    </div>
    <div class="header">
      <h1>АРХИВ</h1>
    </div>
    <div class="arc-container">
      <div v-if="ip" class="main">
        <div class="archieve">
          <nuxt-link
            style="text-decoration: none; color: inherit"
            :to="`../schedule`"
          >
            Расписание мероприятий
          </nuxt-link>
        </div>
        <div v-for="el in ip" :key="el.id" class="events-filter">
          <div class="event-wrapper">
            <div v-for="el2 in el.events" :key="el2.id" class="events">
              <nuxt-link
                style="text-decoration: none; color: inherit"
                :to="`/events/${el2.id}`"
              >
                <div class="event-date">
                  <div class="date-filter">
                    <p class="main-date">
                      {{ el2.start_date.slice(0, 4) }}
                    </p>
                    <p class="main-date">{{ el2.start_date.slice(5, 7) }}.</p>
                  </div>
                </div>
                <div class="event-box">
                  <div class="event-item">
                    <div class="date-time">
                      <div class="date-filter-2">
                        <p class="date">{{ el2.start_date.slice(5, 7) }}</p>
                        <p class="date">{{ el2.start_date.slice(8, 10) }}.</p>
                      </div>
                      <p class="time">
                        {{ el2.start_date.slice(11, 16) }}
                        {{ el2.end_date.slice(11, 16) }}
                      </p>
                    </div>
                    <div class="event-title">
                      {{ el2.title }}
                    </div>
                    <div class="event-speaker">
                      {{ el2.speaker }}
                    </div>
                  </div>
                </div>
              </nuxt-link>
            </div>
          </div>
          <div class="img-filter">
            <img :src="el.event_photo" alt="" />
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
    }
  },
  methods: {
    async event() {
      const ip = await this.$axios.$get('https://smartpoint.me/api/archieve/')
      this.ip = ip
      console.log(ip)
    },
  },
  computed: {
    first() {
      return this.ip[0]
    },
  },
  created() {
    this.event()
  },
}
</script>
<style scoped>
.date-filter-2 {
  display: flex;
  flex-direction: row-reverse;
}
.date-filter {
  display: flex;
  flex-direction: row-reverse;
}
.main-date {
  font-size: 25px;
  font-weight: 800;
  position: relative;
  left: 10vw;
}
.events-filter {
  margin-bottom: 100px;
}
.arc-container {
  margin: 0 auto;
}
@media (min-width: 1201px) {
  .arc-container {
    width: 1038px;
  }
}
@media (min-width: 701px) {
  .date-time {
    justify-content: space-between;
  }
}
@media (max-width: 700px) {
  .arc-container {
    width: 500px !important;
  }
  .img-filter {
  }
  .event-wrapper {
    font-size: 15px;
    font-weight: 700;
  }
}
.event-date {
  position: absolute;
  max-width: 100%;
  width: 200px;
}
.event-wrapper {
  font-size: 1rem;
  font-weight: 600;
  color: #000b22;
  overflow-y: scroll;
  max-height: 39vh;
  font-size: 1rem;
  font-weight: 600;
  color: #000b22;
  text-transform: uppercase;
  max-height: 39vh;
}
.event-box {
  margin-top: 15px;
}
.event-wrapper::-webkit-scrollbar-thumb {
  border: 2px solid white;
  background-color: #ccc;
}
.event-wrapper::-webkit-scrollbar {
  -webkit-appearance: none;
}

.event-wrapper::-webkit-scrollbar:horizontal {
  height: 13px;
}

.event-wrapper::-webkit-scrollbar-thumb {
  border-radius: 6px;
  border: 2px solid white;
  background-color: rgba(29, 29, 82, 0.5);
}
@media (max-width: 1200px) {
  .events-filter:nth-child(even) .main-date {
    left: 0 !important;
  }
  .arc-container {
    width: 700px;
  }
  .events-filter {
    display: block !important;
  }
  .img-filter img {
    padding-left: 10vw;
  }
}
.img-filter img {
  max-width: 100%;
  width: 580px;
}

.main-date {
  display: none;
}
.events-filter:nth-child(2n) {
  flex-direction: row-reverse;
}
.events-filter {
  display: flex;
  justify-content: space-between;
}

.events-filter:nth-child(even) .main-date {
  position: relative;
  bottom: 4vh;
  left: -759px;
}
.events-filter:nth-child(odd) .main-date {
  position: relative;
  bottom: 4vh;
  left: -140px;
}
.events:first-child .main-date {
  display: block;
}
.event-speaker {
  max-width: 390px;
  width: 100%;
}
.event-title {
  padding-top: 10px;
  padding-bottom: 10px;
  max-width: 390px;
  width: 100%;
}
.img-filter {
  text-align: center;

  padding-top: 50px;
}
.event-box {
  display: flex;
}
.events-filter:nth-child(2n) .event-box {
  display: flex;
}
.event-box {
  border-bottom: 2px solid #dedede;
  cursor: pointer;
  padding-top: 15px;
  justify-content: center;
}
.date-time {
  width: 400px;
  display: flex;
}
.nav {
  padding-left: 95px;
  padding-top: 15px;
  justify-content: left;
  display: flex;
  height: 30px;
  background-color: #fff45e;
}
.header {
  padding-bottom: 50px;
  padding-top: 50px;
  font-size: 2rem;
  /* font-weight: 700; */
  font-family: sans-serif;
  font-weight: 500;
  color: #263164;
  line-height: 72px;
  text-transform: uppercase;
  text-align: center;
  background-color: #fff45e;
}
.archieve {
  margin: 50px 100px 50px 0px;
  height: 30px;
  text-align: right;
}
.archieve a {
  margin-right: 20px;
  font-weight: 500;
  font-size: 15px;
  padding: 10px 35px 10px 35px;
  /* text-align: right; */
  /* position: relative; */
  /* left: 77%; */
  text-decoration: none;
  color: #263164;
  border: 1px solid #263164;
  /* top: 104%; */
  /* bottom: -93px; */
}
.main {
  font-family: sans-serif;
  height: 100%;
  width: 100%;
  /* background-image:url('https://smartpoint.me/_nuxt/img/mountain-bg.ca5c441.png'); */
  /* background-size: cover; */
}
</style>
