<template>
  <div class="wrapper">
    <div class="nav">
      <div class="nav-main">
        <nuxt-link style="text-decoration: none; color: inherit" :to="'/'">
          Главная
        </nuxt-link>
      </div>
      <p>></p>
      <div class="nav-event">
        {{ ip.title }}
      </div>
    </div>
    <div class="header">
      <h1>
        {{ ip.title }}
      </h1>
    </div>
    <div class="container">
      <div class="main">
        <div class="events">
          <div class="img-info">
            <div class="event-img">
              <img :src="ip.main_photo" alt="" />
            </div>
            <div class="event-info">
              <div class="date">
                <h3>ДАТА</h3>
                <div class="date-content">
                  <div class="day">
                    {{ ip.start_date }}
                  </div>
                  <div class="time">
                    {{ ip.start_date }}
                    {{ ip.end_date }}
                  </div>
                </div>
              </div>
              <div class="speaker">
                <h3>СПИКЕР</h3>
                <p>
                  {{ ip.speaker }}
                </p>
              </div>
              <button class="reg">Зарегистрироваться</button>
            </div>
          </div>
          <div class="desc">
            <h2>ОПИСАНИЕ</h2>
            <div class="content">
              {{ ip.description }}
            </div>
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
      const ip = await this.$axios.$get(
        `https://smartpoint.me/api/event/${this.id}`
      )
      this.ip = ip
    },
  },
  computed: {
    id() {
      return this.$route.params.id
    },
  },
  created() {
    return this.event()
  },
}
</script>
<style scoped>
.content {
  padding-bottom: 50px;
}
.container {
  margin: 0 auto;
}
@media (min-width: 1201px) {
  .container {
    width: 1200px;
  }
  .img-info {
    display: flex;
  }
}
@media (max-width: 810px) {
  .container {
    width: 500px !important;
  }
  .event-img {
    width: 500px !important;
  }
  .img-info {
    width: 300px !important;
  }
  .main {
    width: 300px !important;
  }
}
@media (max-width: 1200px) {
  .container {
    width: 800px;
  }
}
.desc h2 {
  font-size: 2rem;
  font-weight: 700;
  color: #263164;
  line-height: 43.5px;
  text-transform: uppercase;
  margin-bottom: 12px;
}
* {
  font-family: sans-serif;
}
.reg {
  text-decoration: none;
  width: 285px;
  height: 50px;
  background: #263164;
  box-shadow: 0 10px 20px rgb(38 49 100 / 15%);
  border-radius: 5px;
  font-size: 1.6rem;
  font-weight: 500;
  color: #fff45e;
  transition: all 0.1s;
}
.date h3 {
  font-size: 2rem;
  font-weight: 700;
  color: #263164;
  line-height: 43.5px;
  text-transform: uppercase;
  margin-bottom: 12px;
}
.date {
  font-size: 1rem;
  font-weight: 400;
  color: #000b22;
  line-height: 18.5px;
  margin-bottom: 50px;
  position: relative;
}
.speaker h3 {
  font-size: 2rem;
  font-weight: 700;
  color: #263164;
  line-height: 43.5px;
  text-transform: uppercase;
  margin-bottom: 12px;
}
.speaker {
  margin-bottom: 50px;
  position: relative;
  font-size: 1rem;
  font-weight: 400;
  color: #000b22;
  line-height: 18.5px;
}
.event-info {
  padding: 30px 30px 60px 30px;
  background-color: white;
  box-shadow: 0 10px 30px rgb(138 149 158 / 15%);
  position: relative;
  bottom: 30px;
}
.wrapper {
  z-index: 1;
}
.main {
  z-index: 3;
}
.events {
  position: relative;
  z-index: 3;
  /* width: 1200px; */
  /* margin: 0 auto; */
}
.date-content {
  display: flex;
  align-items: center;
  position: relative;
  margin-right: 60px;
}
.img-info {
  align-items: flex-start;
  justify-content: space-between;
}
.event-img {
  width: 692px;
}
.event-img img {
  position: relative;
  width: 100%;
  bottom: 30px;
}
.nav {
  padding-left: 95px;
  padding-top: 15px;
  justify-content: left;
  display: flex;
  height: 30px;
  background-color: #fff45e;
}
.nav-main a {
  text-decoration: none;
  color: #263164;
  margin-right: 5px;
}
.nav-event {
  margin-left: 5px;
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
.archieve a {
  margin-right: 20px;
  font-weight: 500;
  font-size: 15px;
  padding: 10px 35px 10px 35px;
  /* text-align: right; */
  position: relative;
  left: 77%;
  text-decoration: none;
  color: #263164;
  border: 1px solid #263164;
  /* top: 104%; */
  bottom: -93px;
}
.main {
  height: 100%;
  width: 100%;
  background-image: url('https://smartpoint.me/_nuxt/img/mountain-bg.ca5c441.png');
  background-size: cover;
}
</style>
