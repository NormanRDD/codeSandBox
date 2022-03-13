<template>
  <div id="gallery" class="gallery-wrapper">
    <div v-if="gallery">
      <button class="btn" @click=";(gallery = false), (isBlur = false)">
        x
      </button>
      <div class="gallery-background">
        <div class="gallery-slider">
          <div class="top-slides">
            <button class="prev-btn" @click.prevent="slidePrev">></button>
            <hooper group="group1">
              <slide v-for="el in img" :key="el.id">
                <div class="top-img">
                  <img :src="el.image" alt="" />
                  <!-- <img src="../img/beni.jpg" alt="" /> -->
                </div>
              </slide>
            </hooper>
            <button class="next-btn" @click.prevent="slideNext">></button>
          </div>
          <div class="bot-slides">
            <hooper
              ref="carousel"
              @slide="updateCarousel"
              group="group1"
              :itemsToShow="3"
              :centerMode="true"
            >
              <slide v-for="el in img" :key="el.id">
                <div class="bot-img">
                  <!-- <img src="../img/beni.jpg" alt="" /> -->

                  <img :src="el.image" alt="" />
                </div>
              </slide>
              <!-- <hooper-navigation slot="hooper-addons"></hooper-navigation> -->
            </hooper>
          </div>
        </div>
      </div>
    </div>
    <div v-bind:class="{ blur: isBlur }">
      <div class="header">
        <p class="background-header">ГАЛЛЕРЕЯ</p>
        <h1 class="inner-header">ГАЛЛЕРЕЯ</h1>
      </div>
      <div class="gallery-container">
        <div class="photos">
          <div class="img-wrapper">
            <img
              @click=";(gallery = true), (isBlur = true)"
              src="https://smartpoint.me/_nuxt/img/gallery-1.079817e.jpg"
              alt=""
            />
          </div>
          <div class="img-wrapper">
            <img
              @click=";(gallery = true), (isBlur = true)"
              src="https://smartpoint.me/_nuxt/img/gallery-2.3772fbc.jpg"
              alt=""
            />
          </div>
          <div class="img-wrapper">
            <img
              @click=";(gallery = true), (isBlur = true)"
              src="https://smartpoint.me/_nuxt/img/gallery-3.16e249f.jpg"
              alt=""
            />
          </div>
          <div class="img-wrapper">
            <img
              @click=";(gallery = true), (isBlur = true)"
              src="https://smartpoint.me/_nuxt/img/gallery-4.ae8dba0.jpg"
              alt=""
            />
          </div>
          <div class="mini-photos">
            <div class="mini-top">
              <div class="mini-img">
                <img
                  class="long-img"
                  @click=";(gallery = true), (isBlur = true)"
                  src="https://smartpoint.me/_nuxt/img/gallery-1.079817e.jpg"
                  alt=""
                />
              </div>

              <div class="mini-img">
                <img
                  class="short-img"
                  @click=";(gallery = true), (isBlur = true)"
                  src="https://smartpoint.me/_nuxt/img/gallery-2.3772fbc.jpg"
                  alt=""
                />
              </div>
            </div>
            <div class="mini-bot">
              <div class="mini-img">
                <img
                  class="short-img"
                  @click=";(gallery = true), (isBlur = true)"
                  src="https://smartpoint.me/_nuxt/img/gallery-3.16e249f.jpg"
                  alt=""
                />
              </div>
              <div class="mini-img">
                <img
                  class="long-img"
                  @click=";(gallery = true), (isBlur = true)"
                  src="https://smartpoint.me/_nuxt/img/gallery-4.ae8dba0.jpg"
                  alt=""
                />
              </div>
            </div>
          </div>
        </div>

        <!-- /////////////////////////////hooper//////////////////////////////////// -->
        <!-- /////////////////////////////hooper//////////////////////////////////// -->
      </div>
    </div>
  </div>
</template>
<script>
import {
  Hooper,
  Slide,
  Pagination as HooperPagination,
  Navigation as HooperNavigation,
} from 'hooper'
import 'assets/css/gallery-hooper.css'

export default {
  name: 'App',
  components: {
    Hooper,
    Slide,
    HooperPagination,
    HooperNavigation,
  },
  data() {
    return {
      isBlur: false,
      carouselData: 0,
      ip: '',
      img: '',
      gallery: '',
      hooperSettings2: {
        itemsToShow: 1,
        centerMode: true,
      },
      hooperSettings: {
        itemsToShow: 6.5,
        centerMode: true,
      },
    }
  },
  watch: {
    carouselData() {
      this.$refs.carousel.slideTo(this.carouselData)
    },
  },
  methods: {
    async gal() {
      const ip = await this.$axios.$get('https://smartpoint.me/api/gallery/')
      let arr = []
      for (let i = 0; i < ip.length; i++) {
        if (ip[i].gallery_image.length > 0) {
          for (let j = 0; j < ip[i].gallery_image.length; j++) {
            arr.push(ip[i].gallery_image[j])
          }
        }
      }
      this.img = arr
      // console.log(arr.length)
      // console.log(arr)
      //   ip.forEach(e => {
      //       e.gallery_image.forEach(j => {
      //           arr.push(j)
      //       })
      //   })
    },
    slidePrev() {
      this.$refs.carousel.slidePrev()
    },
    slideNext() {
      this.$refs.carousel.slideNext()
    },
    updateCarousel(payload) {
      this.myCarouselData = payload.currentSlide
    },
  },
  created() {
    this.gal()
  },
}
</script>
<style scoped>
.prev-btn {
  position: relative;
  left: -4%;
  transform: rotateY(180deg);
  font-size: 42px;
  font-family: sans-serif;
  border: 0px;
  height: 3vh;
  color: #fff45e;
  background-color: transparent;
}
.next-btn {
  position: relative;
  font-size: 42px;
  font-family: sans-serif;
  border: 0px;
  height: 3vh;
  color: #fff45e;
  background-color: transparent;
}
li.hooper-slide {
  /* width: 300px !important; */
}

.hooper-container {
  margin: 0 auto;
}
@media (min-width: 1201px) {
  .hooper-container {
    width: 1200px;
  }
}
.gallery-container {
  margin: 0 auto;
}
@media (min-width: 1201px) {
  .next-btn {
    left: -54%;
    top: 19vh;
  }
  .prev-btn {
    top: 19vh;
  }
  .gallery-container {
    width: 1200px;
  }
  .background-header {
    font-size: 13rem;

    left: 30%;
    top: 110px;
  }
  .inner-header {
    font-size: 6rem;

    left: 300px;
    top: -185px;
  }
}
@media (max-width: 800px) {
  .gallery-container {
    width: 500px !important;
  }
  .inner-header {
    left: 60px !important;
    font-size: 3rem !important;
    top: -13px !important;
  }
  .background-header {
    left: 42% !important;
    font-size: 4rem !important;
  }
}
@media (max-width: 1200px) {
  .gallery-container {
    width: 800px;
  }
  .next-btn {
    left: -71%;
    top: 15vh;
  }
  .prev-btn {
    top: 15vh;
  }
  .background-header {
    top: 110px;
    overflow: hidden;
    left: 45%;
    font-size: 9rem;
  }
  .inner-header {
    font-size: 5rem;
    top: -185px;
    left: 167px;
    top: -105px;
  }
}
.mini-top {
  display: flex;
}
.mini-top .mini-img:first-child {
  width: 211px;
  height: 124px;
}
.mini-top .mini-img:first-child img {
  width: 211px;
  height: 124px;
}
.mini-top .mini-img:not(:first-child) {
  width: 124px;
  height: 124px;
}
.mini-top .mini-img:not(:first-child) img {
  width: 124px !important;
  height: 124px !important;
}
.mini-bot {
  margin-top: 25px;
}
.mini-bot .mini-img:first-child {
  width: 124px !important;
  height: 124px !important;
}
.mini-bot .mini-img:first-child img {
  width: 124px !important;
  height: 124px !important;
}
.mini-bot .mini-img:not(:first-child) {
  width: 211px !important;
  height: 124px !important;
}
.mini-bot .mini-img:not(:first-child) img {
  width: 211px !important;
  height: 124px !important;
}

.mini-bot {
  display: flex;
}
.mini-photos {
  display: none;
}
.mini-img:not(:first-child) img {
  /* max-width: 250px; */
  height: auto;
}
.mini-img:first-child {
  width: 370px;
  height: 500px;
}
.mini-img:first-child img {
  width: 370px;
  height: 500px;
}
.mini-img {
  margin-right: 20px;
  width: 250px;
  height: 350px;
  position: relative;
  background-color: #fff45e;
  border-radius: 5px;
  transition: all 0.2s;
}
.mini-img img {
  border-radius: 5%;
}
@media (max-width: 870px) {
  .img-wrapper {
    display: none !important;
  }
  .mini-photos {
    display: block !important;
  }
}
@media (min-width: 1201px) {
  .top-img {
    width: 500px;
    height: 100%;
  }
  .bot-img {
    width: 220px;
  }
}
@media (max-width: 1200px) {
  .top-img {
    width: 300px;
    height: 100%;
  }
  .bot-img {
    width: 120px;
  }
}
@media (max-width: 700px) {
  .prev-btn {
    top: 5vh !important;
  }
  .next-btn {
    top: 5vh !important;
    left: -81% !important;
  }
  .top-img {
    width: 200px !important;
    height: 100%;
  }
  .bot-img {
    width: 70px !important;
  }
}
.top-img img {
  max-width: 100%;
}
.bot-img img {
  width: 100% !important;
}
.bot-slide {
  height: auto;
  width: 150px;
}
.btn-wrapper {
  background-color: red;
}
.btn {
  color: #fff45e;
  background-color: transparent;
  border: none;
  font-size: 25px;
  width: 50px;
  height: 50px;
  cursor: pointer;
  position: fixed;
  font-weight: 700;
  font-family: sans-serif;
  font-size: 34px;
  z-index: 999;
  left: 92%;
  bottom: 84%;
}
.bot-slides {
  top: 15px;
  position: relative;
  right: 20vw;
  width: 100vw;
}
.top-slides {
  /* width: 300px; */
  margin-right: 10px;
  display: flex;
  height: 52%;
  margin-bottom: 50px;
}
.gallery-slider {
  transition: opacity 0.2s ease;
  width: 1200px;
  margin-left: 30vw;
  margin-top: 21vh;
  color: white;
  /* position: fixed; */
  /* top: 190px; */
  /* top: 0; */
  /* left: 0; */
  /* display: table; */
  /* margin: 0 auto; */
  /* z-index: 10; */
  /* margin: 0 auto; */
  /* text-align: center; */
  /* padding-left: 200px; */
  /* height: 100px; */
  /* background-color: aliceblue; */
}
.gallery-background {
  transition: opacity 0.2s ease;
  position: fixed;
  z-index: 5;
  top: 0;
  left: 0;
  width: 100%;
  min-height: 100%;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.8);
  display: table;
}
.gallery-wrapper {
  /* filter: blur(4px); */

  font-family: sans-serif;
  /* overflow: hidden; */
}
.blur {
  filter: blur(4px);
}
.photos {
  justify-content: center;
  display: flex;
}
.img-wrapper img:hover {
  transition: all 0.4s;
  transform: translate(20px, 20px);
}
@media (min-width: 1201px) {
  .img-wrapper:not(:first-child) img {
    max-width: 250px;
    height: auto;
  }
  .img-wrapper:first-child {
    width: 370px;
    height: 500px;
  }
  .img-wrapper:first-child img {
    width: 370px;
    height: 500px;
  }
  .img-wrapper {
    margin-right: 20px;
    width: 250px;
    height: 350px;
    position: relative;
    background-color: #fff45e;
    border-radius: 5px;
    transition: all 0.2s;
  }
  .img-wrapper img {
    border-radius: 5%;
  }
}
@media (max-width: 1200px) {
  .img-wrapper:not(:first-child) img {
    max-width: 175px;
    height: auto;
  }
  .img-wrapper:first-child {
    width: 250px;
    height: 335px;
  }
  .img-wrapper {
    margin-right: 20px;
    width: 175px;
    height: 240px;
    position: relative;
    background-color: #fff45e;
    border-radius: 5px;
    transition: all 0.2s;
  }
  .img-wrapper:first-child img {
    width: 250px;
    height: auto;
  }
}

.inner-header {
  position: relative;
  color: #263164;
  font-weight: 600;
  width: 190px;
}
.background-header {
  font-weight: 700;
  color: transparent;
  -webkit-text-stroke-width: 3px;
  -webkit-text-stroke-color: rgba(52, 52, 52, 0.05);
  position: relative;
  /* width: 675px; */
  transform: translate(-50%, -50%);
}
.gallery-header {
  padding-top: 50px;
}
</style>
