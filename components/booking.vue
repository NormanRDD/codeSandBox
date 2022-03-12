
<template>
<div id="bookingg" class="wrapper">
    <div class="booking-container">
        <div class="header">
            <h1>
                ОНЛАЙН БРОНИРОВАНИЕ
            </h1>
            <div class="nav">
                <div>

            <button class="btn-1">
                Smart Point 1
            </button>
                </div>
                <div>

            <button class="btn-2">
                Smart Point 2
            </button>
                </div>
                <div>

            <button class="btn-3">
                Smart Point 3
            </button>
                </div>
          </div>
        </div>
            <div class="sp1_wrapper">
        
            <div class="booking-wrapper">
                <div class="booking-1">
                <img class="booking-1-img" src="../img/booking/booking1.png" alt="">
            <div @mouseover="office_1 = true" @mouseleave="office_1 = false" class="office office-1">
                <img  src="../img/booking/office1.png" alt="">
                <div  class="office-info" v-if="office_1">   
                <p class="office-info-header">
                    ОФИС 1
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 18
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 72м2
                </p>
                </div>
            </div>
                <!-- <img src="../img/booking/office-1-case.png" alt=""> -->
            <div @mouseover="office_2 = true" @mouseleave="office_2 = false" class="office office-2">
                <img src="../img/booking/office2.png" alt="">
                <div  class="office-info" v-if="office_2">   
                <p class="office-info-header">
                    ОФИС 2  
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 18
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 72,8м2
                </p>
                </div>
            </div>
                <div @mouseover="office_3 = true" @mouseleave="office_3 = false" class="office office-3">
                <img src="../img/booking/office3.png" alt="">
                <div  class="office-info" v-if="office_3">   
                <p class="office-info-header">
                    ОФИС 3 
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 21
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 84,7м2
                </p>
                </div>
            </div>
                <div @mouseover="office_4 = true" @mouseleave="office_4 = false" class="office office-4">
                <img src="../img/booking/office4.png" alt="">
                <div  class="office-info" v-if="office_4">   
                <p class="office-info-header">
                    ОФИС 4  
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 5
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 20м2
                </p>
                </div>
            </div>
                <div @mouseover="office_5 = true" @mouseleave="office_5 = false" class="office office-5">
                <img src="../img/booking/office5.png" alt="">
                <div  class="office-info" v-if="office_5">   
                <p class="office-info-header">
                    ОФИС 5  
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 5
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 20м2
                </p>
                </div>
            </div>
                <div @mouseover="office_6 = true" @mouseleave="office_6 = false" class="office office-6">
                <img src="../img/booking/office6.png" alt="">
                <div  class="office-info" v-if="office_6">   
                <p class="office-info-header">
                    ОФИС 6  
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 7
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 30м2
                </p>
                </div>
            </div>
            <div @mouseover="office_6 = true" @mouseleave="office_6 = false" class="office office-6-2">
                <img src="../img/booking/office6-2.png" alt="">
                <div  class="office-info" v-if="office_6">   
                <p class="office-info-header">
                    ОФИС 6  
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 7
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 30м2
                </p>
                </div>
            </div>
                <div @mouseover="office_7 = true" @mouseleave="office_7 = false" class="office office-7">
                <img src="../img/booking/office7.png" alt="">
                <div  class="office-info" v-if="office_7">   
                <p class="office-info-header">
                    ОФИС 7  
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 3
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 14м2
                </p>
                </div>
            </div>
            <div @mouseover="office_8 = true" @mouseleave="office_8 = false" class="office office-8">
                <img src="../img/booking/office8.png" alt="">
                <div  class="office-info" v-if="office_8">   
                <p class="office-info-header">
                    ОФИС 8  
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 26
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 26м2
                </p>
                </div>
            </div>
                <div @mouseover="office_9 = true" @mouseleave="office_9 = false" class="office office-9">
                <img src="../img/booking/office9.png" alt="">
                <div  class="office-info" v-if="office_9">   
                <p class="office-info-header">
                    ОФИС 9  
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 4
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 16,6м2
                </p>
                </div>
            </div>
            <div @mouseover="office_10 = true" @mouseleave="office_19 = false" class="office office-10">
                <img src="../img/booking/office10.png" alt="">
                <div  class="office-info" v-if="office_10">   
                <p class="office-info-header">
                    ОФИС 10  
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 4
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 17м2
                </p>
                </div>
            </div>
                <div @mouseover="office_11 = true" @mouseleave="office_11 = false" class="office office-11-1">
                <img src="../img/booking/office11-1.png" alt="">
                <div  class="office-info" v-if="office_11">   
                <p class="office-info-header">
                    ОФИС 11  
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 6
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 24м2
                </p>
                </div>
            </div>
            <div @mouseover="office_11 = true" @mouseleave="office_11 = false" class="office office-11-2">
                <img src="../img/booking/office11-2.png" alt="">
                <div  class="office-info" v-if="office_11">   
                <p class="office-info-header">
                    ОФИС 11  
                </p>         
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 6
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 24м2
                </p>
                </div>
            </div>
            <div @mouseover="spStaff = true" @mouseleave="spStaff = false" class="office spStaff">
                <img src="../img/booking/spStaff.png" alt="">
                <div  class="office-info" v-if="spStaff">   
                <p class="office-info-header">
                    Smart Point <br>
                    Staff  
                </p>         
                </div>
            </div>
            <div @mouseover="coworking = true" @mouseleave="coworking = false" class="office coworking">
                <img src="../img/booking/coworking.png" alt="">
                <div  class="office-info" v-if="coworking">   
                <p class="office-info-header">
                    КОВОРКИНГ ЗОНА
                </p>         
                </div>
            </div>
                <div @mouseover="coworking2 = true" @mouseleave="coworking2 = false" class="office coworking2">
                <img src="../img/booking/coworking2.png" alt="">
                <div  class="office-info" v-if="coworking2">   
                <p class="office-info-header">
                    КОВОРКИНГ ЗОНА
                </p>         
                </div>
            </div>
            <div @mouseover="coworking3 = true" @mouseleave="coworking3 = false" class="office coworking3">
                <img src="../img/booking/coworking3.png" alt="">
                <div  class="office-info" v-if="coworking3">   
                <p class="office-info-header">
                    КОВОРКИНГ ЗОНА
                </p>         
                </div>
            </div>
            <div @mouseover="queen = true" @mouseleave="queen = false" class="office queen">
                <img src="../img/booking/queen.png" alt="">
                <div class="office-info" v-if="queen">   
                <p class="office-info-header">
                    QUEEN
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 3
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 15м2
                </p>         
                </div>
            </div>
                <div @mouseover="coldplay = true" @mouseleave="coldplay = false" class="office coldplay">
                <img src="../img/booking/coldplay.png" alt="">
                <div class="office-info" v-if="coldplay">   
                <p class="office-info-header">
                    COLDPLAY
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 3
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 12м2
                </p>         
                </div>
            </div>
                <div @mouseover="muse = true" @mouseleave="muse = false" class="office muse">
                <img src="../img/booking/muse.png" alt="">
                <div class="office-info" v-if="muse">   
                <p class="office-info-header">
                    MUSE
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 3
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 15м2
                </p>         
                </div>
                </div>
                <div @mouseover="kiss = true" @mouseleave="kiss = false" class="office kiss">
                <img src="../img/booking/kiss.png" alt="">
                <div class="office-info" v-if="kiss">   
                <p class="office-info-header">
                    KISS
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 3
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 15м2
                </p>         
                </div>
                </div>
                <div @mouseover="nirvana = true" @mouseleave="nirvana = false" class="office nirvana">
                <img src="../img/booking/nirvana.png" alt="">
                <div class="office-info" v-if="nirvana">   
                <p class="office-header">
                    NIRVANA
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 3
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 15м2
                </p>         
                </div>
                </div>
                <div @mouseover="metallica = true" @mouseleave="metallica = false" class="office metallica">
                <img src="../img/booking/metallica.png" alt="">
                <div class="office-info" v-if="metallica">   
                <p class="office-info-header">
                    METALLICA
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    конференц-зал
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 15м2
                </p>         
                </div>
                </div>
                <div @mouseover="greenDay = true" @mouseleave="greenDay = false" class="office greenDay">
                <img src="../img/booking/greenDay.png" alt="">
                <div class="office-info" v-if="greenDay">   
                <p class="office-info-header">
                    GREENDAY
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 5
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 25м2
                </p>         
                </div>
                </div>
                <div @mouseover="offSpring = true" @mouseleave="offSpring = false" class="office offspring">
                <img src="../img/booking/offspring.png" alt="">
                <div class="office-info" v-if="offSpring">   
                <p class="office-info-header">
                    OFFSPRING
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 6
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 25м2
                </p>         
                </div>
                </div>
                <div @mouseover="blur = true" @mouseleave="blur = false" class="office blur">
                <img src="../img/booking/blur.png" alt="">
                <div class="office-info" v-if="blur">   
                <p class="office-info-header">
                    BLUR
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 3
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 15м2
                </p>         
                </div>
                </div>
                <div @mouseover="beatles = true" @mouseleave="beatles = false" class="office beatles">
                <img src="../img/booking/beatles.png" alt="">
                <div class="office-info" v-if="beatles">   
                <p class="office-info-header">
                    BEATLES
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 3
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 15м2
                </p>         
                </div>
                </div>
                <div @mouseover="deepPurple = true" @mouseleave="deepPurple = false" class="office deepPurple">
                <img src="../img/booking/deepPurple.png" alt="">
                <div class="office-info" v-if="deepPurple">   
                <p class="office-info-header">
                    DEEPPURPLE
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    конференц-зал
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 52м2
                </p>         
                </div>
                </div>
                <!-- <div @mouseover="pinkFloyd = true" @mouseleave="pinkFloyd = false" class="office pinkFloyd-1">
                <img src="../img/booking/pinkFloyd-1.png" alt="">
                <div class="pinkFloyd-info" v-if="pinkFloyd">   
                <p class="pinkFloyd-header">
                    PINKFLOYD
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 13
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 52м2
                </p>         
                </div>
                </div> -->
                <div @mouseover="pinkFloyd = true" @mouseleave="pinkFloyd = false" class="office pinkFloyd-2">
                <img src="../img/booking/pinkFloyd-2.png" alt="">
                <div class="office-info" v-if="pinkFloyd">   
                <p class="office-info-header">
                    PINKFLOYD
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 13
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 52м2
                </p>         
                </div>
                </div>
                <div @mouseover="coworking4 = true" @mouseleave="coworking4 = false" class="office coworking4">
                <img src="../img/booking/coworking4.png" alt="">
                <div class="office-info" v-if="coworking4">   
                <p class="office-info-header">
                    КОВОРКИНГ ЗОНА
                </p>         
                </div>
                </div>
                <div  @mouseover="office12 = true" @mouseleave="office12 = false" class="office office12">
                <img src="../img/booking/office12.png" alt="">
                <div class="office-info" v-if="office12">   
                <p class="office-info-header">
                    ОФИС 12
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    рабочих мест - 12
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 62,7м2
                </p>         
                </div>
                </div>
                <div @mouseover="dimash = true" @mouseleave="dimash = false" class="office dimash">
                <img src="../img/booking/dimash.png" alt="">
                <div class="office-info" v-if="dimash">   
                <p class="office-info-header">
                    DIMASH
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    конференц-зал
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 16м2
                </p>         
                </div>
                </div>
                <div @mouseover="ulytau = true" @mouseleave="ulytau = false" class="office ulytau">
                <img src="../img/booking/ulytau.png" alt="">
                <div class="office-info" v-if="ulytau">   
                <p class="office-info-header">
                    ULYTAU
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    конференц-зал
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 16м2
                </p>         
                </div>
                </div>
                <div @mouseover="a_studio = true" @mouseleave="a_studio = false" class="office a-studio">
                <img src="../img/booking/a-studio.png" alt="">
                <div class="office-info" v-if="a_studio">   
                <p class="office-info-header">
                    A-STUDIO
                </p>
                <p>
                    <img src="../img/booking/office-chair.png" alt="">
                    конференц-зал
                </p>
                <p>
                    <img src="../img/booking/office-field.png" alt="">
                    площадь - 31м2
                </p>         
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
           office_1 : '',
           office_2 : '',
           office_3 : '',
           office_4 : '',
           office_5 : '',
           office_6 : '',
           office_7 : '',
           office_8 : '',
           office_9 : '',
           office_10 : '',
           office_11 : '',
           spStaff : '',
           coworking : '',
           coworking2 : '',
           coworking3 : '',
           queen : '',
           coldplay : '',
           muse : '',
           kiss : '',
           nirvana : '',
           metallica : '',
           greenDay : '',
           offSpring : '',
           blur : '',
           beatles : '',
           deepPurple : '',
           pinkFloyd : '',
           coworking4 : '',
           office12 : '',
           dimash : '',
           ulytau : '',
           a_studio : ''
        }
    }
}
</script>
<style scoped>
.nav{
    display: flex;
    justify-content: center;
}
.wrapper{
    overflow: hidden;    
}
.booking-container{
    width: 1200px;
    margin: 0 auto;
}
img.booking-1-img{
    max-width: 100%;
    height: auto;
}
@media(max-width:1220px){
    .prices-left{
        font-size: 1px;
    }
    .booking-container{
        width: 600px !important;
    }
    .header h1{
        font-size: 40px !important;
    }
}
@media(max-width:820px){
     .prices-container{
        /* font-size: 15px; */
    }
    .btn-1,
    .btn-2,
    .btn-3  {
        margin-bottom: 20px !important;
    }
    .booking-container{
        width: 400px !important;
    }
    .header h1{
        font-size: 30px !important;
    }
    .nav{
        display: block !important;
    }
}
.wrapper{
    font-family: sans-serif;
    background-color: #1D1D1D;
}
.header{
    text-align: center;
}
.header h1{
    padding-top: 156px;
    padding-bottom: 76px;
    font-weight: 700;
    font-size: 60px;
    color: aliceblue;
}
.btn-1,
.btn-2,
.btn-3{
    margin-left: 10px;
    font-weight: 600;
    font-size: 14px;
    padding: 16px 43px 16px 43px;
    background: #FFF45E;
    box-shadow: 0px 10px 20px rgba(191, 191, 191, 0.15);
    border-radius: 5px;
}
.sp1_wrapper{
    font-family: sans-serif;
    background-color: #1D1D1D;
}
.header{
    text-align: center;
}
.header h1{
    padding-top: 156px;
    padding-bottom: 76px;
    font-weight: 700;
    font-size: 60px;
    color: aliceblue;
}
.btn-1,
.btn-2,
.btn-3{
    margin-left: 10px;
    font-weight: 600;
    font-size: 14px;
    padding: 16px 43px 16px 43px;
    background: #FFF45E;
    box-shadow: 0px 10px 20px rgba(191, 191, 191, 0.15);
    border-radius: 5px;
}

.booking-wrapper{
    display: flex;
    justify-content: center;
}
.booking-1{
    width: 1200px;
    text-align: center;
    margin-top: 55px;
    position: relative;
    /* max-width: 100%; */
}
.office:hover{
    opacity: 1;
    transition:all 0.5s;
}
.office{
    width: 115px;
    opacity: 0;
    transition:all 0.5s;
}
.area-wrapper{
    position: relative;
}
.office-1{
    position: absolute;
    bottom: 848px;
    left: 666px;
    transition:all 0.5s;
}
/* .office-1::after{
    content: "ОФИС 1";
    background-image: url('../img/scroll.svg');
    position: absolute;
    left: 138px;
    background-color: white;
    padding: 10px 50px 10px 50px;
} */
.office-2{
    position: absolute;
    bottom: 830px;
    left: 549px;
}
.office-3{
    position: absolute;
    bottom: 828px;
    left: 434px;
}
.office-4{
    position: absolute;
    bottom: 897px;
    left: 348px;
}
.office-5{
    position: absolute;
    bottom: 897px;
    left: 321px;
    width: 51px;

}
.office-6{
    position: absolute;
    bottom: 872px;
    left: 103px;
}
.office-6-2{
    position: absolute;
    bottom: 834px;
    left: 94px;
}
.office-7{
    position: absolute;
    bottom: 785px;
    left: 91px;
}
.office-8{
    position: absolute;
    bottom: 699px;
    left: 86px;
}
.office-9{
    position: absolute;
    bottom: 617px;
    left: 80px;
}
.office-10{
    position: absolute;
    bottom: 564px;
    left: 76px;
}
.office-11-1{
    position: absolute;
    bottom: 502px;
    left: 72px;
}
.office-11-2{
    position: absolute;
    bottom: 443px;
    left: 68px; 
}
.spStaff{
    position: absolute;
    bottom: 313px;
    left: 87px;
}
.coworking{
    position: absolute;
    bottom: 553px;
    left: 177px;
}
.coworking2{
    position: absolute;
    bottom: 436px;
    left: 316px;
}
.coworking3{
    position: absolute;
    bottom: 446px;
    left: 421px;
}
.queen{
    position: absolute;
    bottom: 775px;
    left: 610px;
}
.coldplay{
    position: absolute;
    bottom: 702px;
    left: 610px;
}
.muse{
    position: absolute;
    bottom: 637px;
    left: 575px;
}
.kiss{
    position: absolute;
    bottom: 762px;
    left: 699px;
}
.nirvana{
    position: absolute;
    bottom: 710px;
    left: 700px;
}
.metallica{
    position: absolute;
    bottom: 670px;
    left: 702px;
}
.greenDay{
    position: absolute;
    bottom: 772px;
    left: 772px;  
}
.offspring{
    position: absolute;
    bottom: 725px;
    left: 773px;   
}
.blur{
    position: absolute;
    bottom: 674px;
    left: 751px;   
}
.beatles{
    position: absolute;
    bottom: 674px;
    left: 796px;   
}
.deepPurple{
    position: absolute;
    bottom: 674px;
    left: 902px;   
}
.pinkFloyd-1{
    position: absolute;
    bottom: 674px;
    left: 1000px;   
}
.pinkFloyd-2{
    position: absolute;
    bottom: 674px;
    left: 1056px;   
}
.coworking4{
    position: absolute;
    bottom: 525px;
    left: 855px;  
}
.office12{
    position: absolute;
    bottom: 243px;
    left: 564px;  
}
.dimash{
    position: absolute;
    bottom: 378px;
    left: 543px;  
}
.ulytau{
    position: absolute;
    bottom: 378px;
    left: 587px; 
}
.a-studio{
    position: absolute;
    bottom: 57px;
    left: 439px; 
}
/* /////////////////////pop-up//////////////////////// */
.office-info
{
    position: absolute;
    padding: 20px 40px 20px 20px;
    min-width: 204px;
    background-color: #fff;
    border-radius: 5px;
    top: 20px;
    left: calc(100% + 20px);
    text-align: left;
    /* display: none; */
    transition: all 0.4s;
    list-style: none;
    font-weight: 500;
    font-size:15px;
    /* opacity: 0; */
    /* visibility: hidden; */
}
/* .office-1-info,
.office-2-info:hover{
    transition: 1s;
} */

.office-info-header
{
    color: #263164;
    font-size:17px;
    margin-bottom: 10px;
    position: relative;
    font-weight: 600;
}
p img{
    margin-right: 10px;
    
}
</style>