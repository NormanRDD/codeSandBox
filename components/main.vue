<template>
    <div class="main">
        <div class="background">

        </div>
        <div class="thesis">
            <img class="pentagon-logo" src="../img/pentagon.png" alt="">
            <h2 class="h2">
                ПРОСТАНСТВО ДЛЯ РАЗУМНЫХ <br>
                ТЕХНОЛОГИЙ <br>
                И КРЕАТИВНЫХ РЕШЕНИЙ
            </h2>
        </div>
        <div class="scroll">
            <a href="#">
                <img src="../img/scroll.png" alt="">
            </a>
        </div>
    </div>
    
</template>
<style scoped>
.main{
    height: 95vh;
}
*{
    /* overflow: hidden; */
}
.h2{
    position: relative;
    bottom: 340px;
}
.scroll{
    z-index: 1;
    position: relative;
    text-align: center;
    top: 34vh;;
    /* margin-top: 200px; */
}
.pentagon-logo{
    z-index: 2;
    position: relative;
    bottom: -115px;
    top: -78px;
    right: 1px;
    width: 350px;
}
.thesis{
    color: #FFF45E;
    z-index: 1;
    position: relative;
    text-align: center;
    /* margin-top: 262px; */
    top: 30vh;
    height: 50vh;
    font-family: sans-serif;
    font-weight: 700;
    font-size: 28px;
}
.background{
    background-image: url('../img/back.png');
    background-size: cover;
    z-index: 0;
    top: 0px;
    /* z-index: 0; */
    position:absolute;
    width: 100%;
    height: 100%;
}
</style>