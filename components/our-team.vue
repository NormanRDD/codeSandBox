<template>
  <div id="our-team" class="wrapper">
      <div class="header">
        <p class="background-header">НАША КОМАНДА</p>
        <h1 class="inner-header">НАША КОМАНДА</h1>
      </div>
    <div class="team-container">
      <hooper ref="carousel" :settings="hooperSettings">
        <slide class="slide" v-for="el in ip" :key="el.id">
          <div class="slide-wrapper" v-if="ip">
            <img class="slide-img" :src="el.card_image" alt="" />
            <div class="name-wrapper">
              <p class="slide-name">{{ el.name }}</p>
              <p class="slide-role">{{ el.role }}</p>
            </div>
          </div>
        </slide>
      </hooper>
      <div class="btns">
        <button class="btn-prev" @click.prevent="slidePrev">
          <svg
            width="40"
            height="28"
            viewBox="0 0 40 28"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M0.244141 14.5888L12.7441 27.0888C13.0697 27.4144 13.597 27.4144 13.9225 27.0888C14.248 26.7633 14.248 26.236 13.9225 25.9105L2.845 14.833L39.1666 14.833C39.6273 14.833 40 14.4603 40 13.9996C40 13.539 39.6273 13.1663 39.1666 13.1663L2.845 13.1663L13.9225 2.08885C14.248 1.7633 14.248 1.23596 13.9225 0.910494C13.7598 0.747759 13.5465 0.666353 13.3333 0.666353C13.1201 0.666353 12.9069 0.747759 12.7441 0.910494L0.244061 13.4105C-0.0814056 13.736 -0.0814056 14.2633 0.244141 14.5888Z"
              fill="#FFF45E"
            />
          </svg>
        </button>
        <button class="btn-next" @click.prevent="slideNext">
          <svg
            width="40"
            height="28"
            viewBox="0 0 40 28"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M0.244141 14.5888L12.7441 27.0888C13.0697 27.4144 13.597 27.4144 13.9225 27.0888C14.248 26.7633 14.248 26.236 13.9225 25.9105L2.845 14.833L39.1666 14.833C39.6273 14.833 40 14.4603 40 13.9996C40 13.539 39.6273 13.1663 39.1666 13.1663L2.845 13.1663L13.9225 2.08885C14.248 1.7633 14.248 1.23596 13.9225 0.910494C13.7598 0.747759 13.5465 0.666353 13.3333 0.666353C13.1201 0.666353 12.9069 0.747759 12.7441 0.910494L0.244061 13.4105C-0.0814056 13.736 -0.0814056 14.2633 0.244141 14.5888Z"
              fill="#FFF45E"
            />
          </svg>
        </button>
      </div>
    </div>
  </div>
</template>
<script>
import { Hooper, Slide } from 'hooper'
import 'assets/css/hooper.css'
export default {
  name: 'App',
  components: {
    Hooper,
    Slide,
  },
  data() {
    return {
      ip: '',
      hooperSettings: {
        itemsToShow: 1,
        breakpoints: {
          900: {
            itemsToShow: 2,
          },
          1200: {
            itemsToShow: 3,
          },
        },
      },
    }
  },
  watch: {
    carouselData() {
      this.$refs.carousel.slideTo(this.carouselData)
    },
  },
  methods: {
    async com() {
      const ip = await this.$axios.$get('https://smartpoint.me/api/our-team/')
      this.ip = ip
    },
    slidePrev() {
      this.$refs.carousel.slidePrev()
    },
    slideNext() {
      this.$refs.carousel.slideNext()
    },
  },
  created() {
    return this.com()
  },
}
</script>
<style scoped>
.slide-wrapper{
  text-align: center;
}
.team-container {
  margin: 0 auto;
}
@media (min-width: 1201px) {
  .team-container {
    width: 1200px;
  }
}
@media (max-width: 1200px) {
  .background-header{
    font-size: 6rem !important;
    left: 60% !;
  }
  .inner-header{
    top: -83px !important;
  }
}
@media(max-width:600px){
    .inner-header{
    font-size: 2rem !important;
    top: -53px !important;
  }
}
@media (max-width: 900px) {
  .btns{
    left: 35% !important;
  }
  .team-container {
    width: 500px;
  }
  .background-header{
    font-size: 5rem !important;
    left: 55% !important;
  }
  .inner-header{
    font-size: 3rem !important;
    top: -53px !important;
  }
}
hooper {
  width: 100px;
  position: relative;
  box-sizing: border-box;
  width: 95% !important;
  margin: 0px 30px 0px 30px !important;
  /* margin-right: 1000px; */
  /* height: 200px; */
}
.name-wrapper {
  color: #263164;
  background-color: #fff45e;
  padding: 20px;
  width: 320px;
  margin: 0 auto;
  position: relative;
  right: 10px;
  bottom: 5px;
  border-radius: 10px;
}
.btn-prev {
  background-color: #1d1d1d;
  border: none;
}
.btn-next {
  background-color: #1d1d1d;
  border: none;
  padding-bottom: -13px;
  position: relative;
  transform: rotate(180deg);
  top: -5px;
  left: 10px;
}
.btns {
  position: relative;
  top: 36px;
  width: 90px;
  left: 80%;
}
.slide-img {
  display: hidden;
  width: 315.667px;
  margin-right: 20px;
}
.slide-name {
  font-size: 1.2rem;
  font-weight: 600;
  color: #263164;
}
.wrapper {
  padding-bottom: 220px;
  font-family: sans-serif;
  padding-top: 100px;
  margin-top: 100px;
  background-color: #1d1d1d;
  height: 78vh;
}
.inner-header {
  position: relative;
  font-size: 3rem;
  color: #fff;
  font-weight: 600;
  left: -25px;
  top: -100px;
  text-align: center;
  font-family: sans-serif;
  padding-bottom: 20px;
}
.header {
  overflow: hidden;
}
.background-header {
  overflow: hidden;
  font-size: 7rem;
  white-space: nowrap;
  font-weight: 700;
  color: transparent;
  -webkit-text-stroke-width: 3px;
  -webkit-text-stroke-color: hsla(0, 0%, 100%, 0.05);
  position: relative;
  left: 55%;
  top: 59px;
  /* width: 100px; */
  transform: translate(-50%, -50%);
}
</style>
