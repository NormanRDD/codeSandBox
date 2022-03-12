<template>
<div class="benefits-wrapper">
    <h3>
        Преимущества
    </h3>
    <div class="list">
        <div class="box">
  <div class="box-inner">
    <div class="box-front">
        <div class="box-front-inner" v-if="ip">
       <img :src="community.card_image" alt="">
        <p v-if="ip">
        {{community.card_title}}
        </p>
        </div>
    </div>
    <div class="box-back">
        <div class="back-inner">
            <div class="p-wrapper">
             <p v-if="ip">
                 {{community.card_title}}
             </p>
            </div>
            <div v-if="ip">
            <ul v-for="el in community.inside_card_text" :key="el.id" >
                <li v-if="ip">
                    {{el.inside_card_text}}
                </li>
            </ul>
            </div>
        </div>
    </div>
  </div>
        </div>

        <div class="box">
  <div class="box-inner">
    <div class="box-front">
        <div class="box-front-inner" v-if="ip">
         <img :src="services.card_image" alt="">
        <p v-if="ip">
           {{services.card_title}}
        </p>
        </div>
    </div>
    <div class="box-back">
        <div class="back-inner">
            <div class="p-wrapper">
             <p v-if="ip">
                 {{services.card_title}}
                 </p>
            </div>
           <div v-if="ip">
            <ul v-for="el in services.inside_card_text" :key="el.id" >
                <li v-if="ip">
                    {{el.inside_card_text}}
                </li>
            </ul>
            </div>
        </div>
    </div>
  </div>
        </div>
          <div class="box">
  <div class="box-inner">
    <div class="box-front">
        <div class="box-front-inner" v-if="ip">
       <img :src="infra.card_image" alt="">
        <p v-if="ip">
            {{infra.card_title}}
        </p>
        </div>
    </div>
    <div class="box-back">
        <div class="back-inner">
            <div class="p-wrapper">
           <p v-if="ip">
            {{infra.card_title}}
        </p>
            </div>
            <div v-if="ip">
            <ul v-for="el in infra.inside_card_text" :key="el.id" >
                <li v-if="ip">
                    {{el.inside_card_text}}
                </li>
            </ul>
          </div>
        </div>
    </div>
  </div>
        </div>
     </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            ip:''
        }
    },
    methods:{
        async fetchSomething(){
            const ip = await this.$axios.$get(`https://smartpoint.me/api/advantages/`)
            this.ip = ip
        }
    //     async asyncData({ $axios }) {
    //     let ip 
    //     ip = await $axios.$get('http://194.146.43.119/api/categories/')
    //     return { ip }
    //   }
    },
    computed: {
      infra(){
      return this.ip[0]
    },
      services(){
      return this.ip[1]
    },
    community(){
      return this.ip[2]
    }
  },
        created(){
            // this.exactImg()
            this.fetchSomething()
        }
}
</script>
<style scoped>

ul li{
    list-style: none;
}

*{
    /* overflow: hidden; */
}
.benefits-wrapper{
    overflow: hidden;
    text-align: center;
    padding-bottom: 150px;
}
.back-inner{
    padding: 15px;
}
.box-front-inner{
    padding-top: 89px;
}
@media(max-width:1280px){
    .box{
        width: 200px !important;
    }
}
@media(max-width: 860px){
    .p-wrapper{
        padding-top: 50px;
    }
         .list{
        display: inline-block !important;
    }
    .box-front-inner{
        padding-top: 30px !important;
    }
    .box-front{
        height: 150px !important; 
    }
    .box-back{
        display:block;
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    }
    .box{
        margin-bottom: 200px;
    }
}
.box {
  font-family: sans-serif;
  background-color: transparent;
  width: 300px;
  height: 300px;
  perspective: 1000px;
  /* text-align: center; */
}

.box-inner {
  /* position: relative; */
  width: 120%;
  height: 100%;
  text-align: center;
  transition: transform 0.6s;
  transform-style: preserve-3d;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
}
@media(min-width: 860px){
    .box:hover .box-inner {
      transform: rotateY(180deg);
    }
    .box-back{
         transform: rotateY(180deg);
    }
    .box-front,
    .box-back{
        position: absolute;
    }
}
.box-front, .box-back {
  width: 100%;
  height: 100%;
  /* -webkit-backface-visibility: hidden; */
  backface-visibility: hidden;
}


.box-front {
  font-size: 22px;
  font-weight: 600;
  /* padding: 100px 150px 100px 150px; */
  background-color: #FFF45E;
  color: #263164;
  /* color: ; */
}

.box-back {
  /* display: inline-block; */
  /* position: relative !important; */
  background-color: white;
  color: black;
  top: 50px;
  /* transform: rotateY(180deg); */
}
.p-wrapper{
    font-size: 1.5rem;
    font-weight: 600;
    color: #263164;
    margin-bottom: 20px;
}
/* .p-border{
    width: 100px;
    border-bottom: 2px solid black;
    margin-left: 46px;
} */

h3{
    font-family: sans-serif;
    padding-top: 63px;
    padding-bottom: 60px;
}
.wrapper{
    text-align: center;
    padding-bottom: 120px;
}
.list{
    display: flex;
    justify-content: space-around;
    /* text-align: center; */
    /* align-items: center; */
    /* margin-left: ; */
}

</style>