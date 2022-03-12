<template>
  <div id="community" class="wrapper">
    <div class="community-container">
      <div class="header">
        <p class="background-header">КОММЬЮНИТИ</p>
        <h1 class="inner-header">КОММЬЮНИТИ</h1>
      </div>
      <hooper ref="carousel" :settings="hooperSettings">
        <slide class="slide" v-for="el in ip" :key="el.id">
          <div class="img-wrapper" v-if="ip">
            <img class="slide-img" :src="el.company_card_image" alt="" />
            <p class="slide-name">{{ el.company_name }}</p>
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
              d="M0.244141 14.5891L12.7441 27.0891C13.0697 27.4146 13.597 27.4146 13.9225 27.0891C14.248 26.7635 14.248 26.2362 13.9225 25.9107L2.845 14.8332L39.1666 14.8332C39.6273 14.8332 40 14.4605 40 13.9999C40 13.5392 39.6273 13.1665 39.1666 13.1665L2.845 13.1665L13.9225 2.08909C14.248 1.76355 14.248 1.23621 13.9225 0.910737C13.7598 0.748003 13.5465 0.666597 13.3333 0.666597C13.1201 0.666597 12.9069 0.748003 12.7441 0.910737L0.244062 13.4107C-0.0814068 13.7362 -0.0814062 14.2635 0.244141 14.5891Z"
              fill="#263164"
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
              d="M0.244141 14.5891L12.7441 27.0891C13.0697 27.4146 13.597 27.4146 13.9225 27.0891C14.248 26.7635 14.248 26.2362 13.9225 25.9107L2.845 14.8332L39.1666 14.8332C39.6273 14.8332 40 14.4605 40 13.9999C40 13.5392 39.6273 13.1665 39.1666 13.1665L2.845 13.1665L13.9225 2.08909C14.248 1.76355 14.248 1.23621 13.9225 0.910737C13.7598 0.748003 13.5465 0.666597 13.3333 0.666597C13.1201 0.666597 12.9069 0.748003 12.7441 0.910737L0.244062 13.4107C-0.0814068 13.7362 -0.0814062 14.2635 0.244141 14.5891Z"
              fill="#263164"
            />
          </svg>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import { Hooper, Slide } from 'hooper'
import 'assets/css/community.css'
export default {
  name: 'App',
  components: {
    Hooper,
    Slide,
  },
  data() {
    return {
      hooperSettings: {
        itemsToShow: 1,
        breakpoints: {
          700: {
            itemsToShow: 2,
          },
          1200: {
            itemsToShow: 3,
          },
        },
      },
      ip: '',
    }
  },
  methods: {
    async com() {
      const ip = await this.$axios.$get('https://smartpoint.me/api/community/')
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

@media (min-width: 1200px) {
  .community-container {
    width: 1200px;
    margin: 0 auto;
  }
}
@media (max-width: 1200px) {
  .community-container {
    width: 700px;
    margin: 0 auto;
  }
}
@media (max-width: 700px) {
  .community-container {
    width: 400px;
    margin: 0 auto;
  }
}
/* @media (min-width: 1200px) {
  .community-container {
    width: 700px;
  }
} */
.header {
  overflow: hidden;
}
.inner-header {
  position: relative;
  font-size: 3rem;
  color: #263164;
  font-weight: 600;
  left: 0px;
  /* bottom: 211px; */
  top: -100px;
  text-align: center;
  font-family: sans-serif;
  padding-bottom: 20px;
}
.background-header {
  overflow: hidden;
  font-size: 7rem;
  white-space: nowrap;
  font-weight: 700;
  color: transparent;
  -webkit-text-stroke-width: 3px;
  -webkit-text-stroke-color: rgba(52, 52, 52, 0.05);
  position: relative;
  left: 77%;
  top: 59px;
  /* width: 100px; */
  transform: translate(-50%, -50%);
}
.slide {
  margin: 0 20px;
}
.slide-name {
  font-size: 1.2rem;
  font-weight: 600;
  color: #263164;
}
.btns {
  position: relative;
  top: 36px;
  width: 90px;
  left: 80%;
}
.wrapper {
  background-color: #f1f1f1;
  /* margin-bottom: 100px; */
  height: 800px;
  font-family: sans-serif;
}
.slide-img {
  display: hidden;
  height: auto;
  max-width: 100%;
}
.slide-img::after {
  /* display: block; */
}
.btn-prev {
  background-color: #f1f1f1;
  border: none;
}
.btn-next {
  background-color: #f1f1f1;
  border: none;
  padding-bottom: -13px;
  position: relative;
  transform: rotate(180deg);
  top: -5px;
  left: 10px;
}
</style>
