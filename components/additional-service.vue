<template>
  <div class="wrapper">
    <div class="header">
      <p class="background-header">ДОПОЛНИТЕЛЬНЫЕ УСЛУГИ</p>
      <h1 class="inner-header">ДОПОЛНИТЕЛЬНЫЕ УСЛУГИ</h1>
    </div>
    <div class="additional-container">
      <div v-if="ip" class="list">
        <div v-for="el in ip" :key="el.id" class="item">
          <img :src="el.card_image" alt="" />
          <h3>{{ el.title }}</h3>
          <p>{{ el.price }}</p>
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
    async fetchSomething() {
      const ip = await this.$axios.$get(
        `https://smartpoint.me/api/additional-services/`
      )
      this.ip = ip
    },
  },
  created() {
    this.fetchSomething()
  },
}
</script>
<style scoped>
.additional-container {
}
@media (min-width: 1200px) {
  .additional-container {
    width: 1200px;
    margin: 0 auto;
  }
}
.list {
  margin-top: 200px;
  grid-template-columns: repeat(3, 224px);
  grid-row-gap: 90px;
  justify-content: space-between;
  display: grid;
  /* padding-bottom: 50px; */
  /* margin-left: 50px; */
  /* margin-right: 50px; */
  /* display: flex; */
}
@media (max-width: 760px) {
  .header{
        position: relative;
    bottom: 169px;
    padding-top: 80px;
    padding-bottom: 50px;
  }
  .list {
    justify-content: center;
    grid-row-gap: 60px;
    grid-template-columns: repeat(1, 224px);
    width: 500px;
    margin: 0 auto;
  }
  .inner-header {
    font-size: 2rem !important;
    top: 150px !important;
  }
  .background-header {
    font-size: 4rem !important;
    top: 244px !important;
  }
}
.item h3 {
}
.item p {
  /* float: right; */
}
.item img {
  width: 60px;
  height: 60px;
}
.item:not(:last-child) {
  /* float: left; */
}
.item:last-child {
  /* margin-bottom: 100px; */
}
.item {
  padding-bottom: 100px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: white;
  /* width: 451px; */
}
.wrapper {
  background-color: #1d1d1d;
  font-family: sans-serif;
}
.inner-header {
  position: relative;
  font-size: 3rem;
  color: white;
  font-weight: 600;
  /* bottom: 211px; */
  top: 88px;
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
  -webkit-text-stroke-color: rgba(52, 52, 52, 0.658);
  position: relative;
  left: 45%;
  top: 244px;
  /* width: 100px; */
  transform: translate(-50%, -50%);
}
</style>
