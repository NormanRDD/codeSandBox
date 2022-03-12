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
      <div style="cursor: pointer" class="nav-schedule">Расписание событий</div>
    </div>
    <div class="header">
      <h1>РАСПИСАНИЕ СОБЫТИЙ</h1>
    </div>
    <div class="main">
      <div class="events"></div>
      <div class="archieve">
        <nuxt-link
          style="text-decoration: none; color: inherit"
          :to="`schedule/archieve`"
        >
          Архив
        </nuxt-link>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      ip: '',
      isActive: undefined,
    }
  },
  watch: {
    '$route.path'() {
      if (this.$route.path == `/Events/schedule`) {
        this.isActive = true
      } else {
        this.isActive = false
      }
    },
  },
  mounted() {
    console.log(this.isActive)
  },
}
</script>
<style scoped>
.wrapper {
  overflow: hidden;
  height: 100vh;
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
