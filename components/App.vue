<template>
    <div class="app">
        <carousel>
            
            <carousel-slide v-for="slide in slides" :key="slide"  class="carousel-slider">
                <div>
                <img :src="slide" :alt="slide">
                </div>
                <div>
                <img :src="first" :alt="slide">
                </div>
                <div>
                <img :src="second" :alt="slide">
                </div>
                <!-- <img :src="slide" :alt="slide"> -->
                <!-- <img :src="slide" :alt="slide"> -->
                <!-- <img :src="slide" :alt="slide"> -->
                <!-- <img :src="slide" :alt="slide"> -->
                <!-- <img :src="first" :alt="slide"> -->
                <!-- <img :src="second" :alt="slide"> -->
            </carousel-slide>
        </carousel>
    </div>    
</template>

<script>
import Carousel from '../components/Carousel.vue';
import CarouselSlide from '../components/CarouselSlide';

export default {
    data(){
        return {
            slides: [
                'https://picsum.photos/id/230/600/300',
                'https://picsum.photos/id/231/600/300',
                'https://picsum.photos/id/232/600/300',
                'https://picsum.photos/id/233/600/300',
                'https://picsum.photos/id/234/600/300',
                'https://picsum.photos/id/235/600/300',
                'https://picsum.photos/id/236/600/300',
            ]
        }
    },

    components : {
        Carousel : Carousel,
        CarouselSlide : CarouselSlide,
    },
    computed:{
         first(){
            return this.slides[1]
        },
        second(){
            return this.slides[2]
        }
    }
}
</script>

<style scoped>
    .app {
        display:flex;
        justify-content: center;
    }
    .carousel {
        position:relative;
        overflow: hidden;
        width:800px;
        height:500px;
        z-index:10;
    }
    .btn {
        padding:5px 10px;
        background-color:rgba(0,0,0,0.5);
        border:1px solid transparent;
        margin:5px 10px;
        color:#FFF;
        height:50px;
        width:50px;
        position:absolute;
        margin-top:-25px;
        z-index:2;
    }
    .btn:hover {
        cursor: pointer;
    }
    .btn:focus{
        outline:none;
    }
    /* .btn-next {
        top:50%;
        right:0;
    }
    .btn-prev {
        top:50%;
        left:0;
    } */
    .carousel-slider {
        display: flex;
        /* position:absolute; */
        top:0;
        left:0;
        bottom:0;
        right:0;
    }
    .carousel-slider img {
        width:100%;
        height:100%;
    }

</style>