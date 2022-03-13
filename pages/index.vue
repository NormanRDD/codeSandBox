<template>
  <div>
    <!-- <App/> -->
    <!-- <Header /> -->
    <!-- <Main /> -->
    <!-- <Offer /> -->
    <!-- <About-us /> -->
    <!-- <Benefits /> -->
    <!-- <Community /> -->
    <!-- <Booking /> -->
    <!-- <Prices /> -->
    <!-- <Coworking-price /> -->
    <!-- <Additional-service/> -->
    <!-- <Events/> -->
    <!-- <Space/> -->
    <!-- <News-section/> -->
    <Gallery/>
    <!-- <Our-team/> -->
    <!-- <Carousel/> -->
    <!-- <CarouselSlide/> -->
    <!-- <Slider-with-big-picture/> -->
    <!-- <Svis/> -->
  </div>
</template>

<script>
// Vue.use(require('vue-moment'));
import additionalService from '~/components/additional-service.vue'
import Community from '~/components/community.vue'
import OurTeam from '~/components/our-team.vue'

export default {
  components: { additionalService, Community, OurTeam },
  // layout:'header',
  // layout:'sp1map',
  // layout:'sp1_map',
  name: 'IndexPage',
}
</script>
<style>
body {
  /* overflow-x: hidden; */
}
* {
  /* overflow: hidden; */
  font-family: sans-serif;
  scroll-behavior: smooth;
}
</style>
