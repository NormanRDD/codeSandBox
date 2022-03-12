<template>
<div class="body">

    <div class="id-wrapper">
    <div class="id-header">
        <h1>НОВОСТИ</h1>
    </div>
         <p v-if="ip">
            {{ip.created_at}}
        </p>
    <div class="id">
    <h3 v-if="ip">
        {{ip.title}}
    </h3>
         <div class="id-text" v-if="ip">
           {{ip.text}}
           {{ip.mini_text}}
         </div>
       </div>
    </div>
</div>
</template>
<script>
export default {
  data(){
      return{
          ip: '',
          isActive: undefined
        } 
   },
     computed: {
            id () {
                return this.$route.params.id
            }
    },
        methods:{
                async fetchSomething(){
                const ip = await this.$axios.$get(`https://smartpoint.me/api/news/${this.id}/`)
                this.ip = ip
        }
        },
        created(){
            this.fetchSomething()
         }
}
</script>
<style>
.id-wrapper p{
    text-align: right;
    margin-right: 273px;
}
.id{
    background-image: url('https://smartpoint.me/_nuxt/img/mountain-bg.ca5c441.png');
    }
.id{
    margin: 0 auto;
    width: 1000px;
    text-align: start;
    font-size:20px ;
}
p.place-p ,
p.lang-p {
    margin: 0;
}
body{
    margin: 0;
    padding: 0;
    /* font-family: sans-serif;  */
}
h1{
    margin: 0;
}
.id h3{
    width: 500px;
    font-size: 25px;
    font-weight: 600;
    color: #263164;
    line-height: 42.95px;
    margin-bottom: 20px;
}
.id-header{
    background-color: #fff45e;
    font-size: 25px;
    font-weight: 700;
    color: #263164;
    line-height: 72px;
    text-transform: uppercase;
    text-align: center;
    padding-bottom: 30px;
}

</style>