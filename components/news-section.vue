<template>
  <div id="news" class="wrapper">
    <div class="news-header">
      <div class="background-header">НОВОСТИ</div>
      <div class="inner-header">НОВОСТИ</div>
    </div>
    <div class="news-container">
      <div v-if="ip" class="news-wrapper">
        <nuxt-link
          style="text-decoration: none; color: inherit"
          :to="`news/${ip[0].id}`"
        >
          <div v-if="ip" class="news news-1">
            <img class="news-image" :src="ip[0].main_photo" alt="" />
            <p v-if="ip">
              {{ ip[0].created_at }}
            </p>
            <h3 v-if="ip">
              {{ ip[0].title }}
            </h3>
            <!-- <div class="text" v-if="ip">
              {{ ip[0].text }}
            </div> -->
            <div class="text" v-if="ip" v-html="ip[0].text"></div>
          </div>
        </nuxt-link>
        <nuxt-link
          style="text-decoration: none; color: inherit"
          :to="`news/${ip[1].id}`"
        >
          <div v-if="ip" class="news news-2">
            <img class="news-image" :src="ip[1].main_photo" alt="" />
            <p v-if="ip">
              {{ ip[1].created_at }}
            </p>
            <h3 v-if="ip">
              {{ ip[1].title }}
            </h3>
            <div class="text" v-if="ip">
              {{ ip[1].mini_text }}
            </div>
          </div>
        </nuxt-link>
        <nuxt-link
          style="text-decoration: none; color: inherit"
          :to="`news/${ip[2].id}`"
        >
          <div v-if="ip" class="news news-3">
            <img class="news-image" :src="ip[2].main_photo" alt="" />
            <p v-if="ip">
              {{ ip[2].created_at }}
            </p>
            <h3 v-if="ip">
              {{ ip[2].title }}
            </h3>
            <div class="text" v-if="ip">
              {{ ip[2].text }}
            </div>
          </div>
        </nuxt-link>
        <nuxt-link
          style="text-decoration: none; color: inherit"
          :to="`news/${ip[3].id}`"
        >
          <div v-if="ip" class="news news-4">
            <img class="news-image" :src="ip[3].main_photo" alt="" />
            <p v-if="ip">
              {{ ip[3].created_at }}
            </p>
            <h3 v-if="ip">
              {{ ip[3].title }}
            </h3>
            <div class="text" v-if="ip">
              {{ ip[4].text }}
            </div>
          </div>
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
    }
  },
  methods: {
    async fetchSomething() {
      const ip = await this.$axios.$get(`https://smartpoint.me/api/news/`)
      this.ip = ip
    },
  },
  created() {
    this.fetchSomething()
  },
}
</script>
<style scoped>
.news-container {
  margin: 0 auto;
}
@media (min-width: 1201px) {
  .news-container {
    width: 1200px;
  }
}
@media (max-width: 1200px) {
  .news.news-3,
  .news.news-4 {
    display: none;
  }
  .news-wrapper {
    justify-content: center;
  }
  .news-container {
    width: 700px;
  }
}
@media (max-width: 750px) {
  .news-container {
    width: 450px;
  }
  .news.news-2 {
    display: none;
  }
  .background-header {
    margin-left: 10% !important;
    font-size: 6rem !important;
  }
  .inner-header {
    font-size: 4rem !important;
    margin-top: -155px !important;
  }
}
.news:hover {
  font-weight: 700;
  transition: 0.5s;
  transform: rotateZ(-5deg);
}

.news p,
h3 {
  margin-bottom: 10px;
}
.news-header {
  /* margin:0 auto */
  padding-right: 100px;
}
.text {
  text-overflow: ellipsis;
  overflow: hidden;
  /* -ms-line-clamp: 2; */
  -webkit-line-clamp: 5;
  line-clamp: 5;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  font-size: 1.6pem;
  line-height: 19px;
}
.wrapper {
  font-family: sans-serif;
  margin-bottom: 30px;
  overflow: hidden;
}
.news-wrapper {
  display: flex;
  align-items: flex-start;
}
.news {
  width: 269px;
  margin-right: 30px;
}
.inner-header {
  font-size: 6rem;
  color: #263164;
  /* left: 283px; */
  font-weight: 600;
  top: -6px;
  margin-left: 52px;
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
.news-image {
  max-width: 100%;
  height: auto;
}
</style>
