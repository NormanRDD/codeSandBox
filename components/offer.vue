<template>
  <div class="caption-wrapper">
    <span class="line-top">
      <!-- <h1 class="caption"> -->
      Работайте 24/7 в комфортном
      <!-- </h1> --> </span
    ><br />
    <span class="line-bot">
      <!-- <h1 class="caption" > -->
      коворкинг - пространстве
      <!-- </h1> -->
    </span>
    <button class="test-btn">
      <p class="test-btn-thesis">Тест драйв SmArt.Point</p>
    </button>
  </div>
</template>
<style scoped>
.caption-wrapper {
  padding: 100px 0px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #f1f1f1;
}
.test-btn {
  width: 350px;
  position: relative;
  background-color: #263164;
  padding: 15px 55px 15px 55px;
  border-radius: 10px;
  margin-left: 0%;
  margin-top: 30px;
  margin-bottom: 30px;
  border: 0px;
}
.test-btn:hover {
  background-color: #354074;
  transition: 0.3s;
}
.test-btn-thesis {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 16px;
  color: #fff45e;
}
.caption {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 30px;
  color: #263164;
  text-align: center;
  padding-top: 100px;
  z-index: 1;
  position: relative;
  /* margin-bottom: 100px; */
}
span {
  position: relative;
  z-index: 2;
  font-size: 50px;
  font-weight: 500;
  color: #263164;
}
span:before {
  content: '   ';
  position: absolute;
  z-index: -1;
  left: -9px;
  top: 38px;
  width: 105%;
  height: 23px;
  background-color: #fff45e;
}
/* .line-1{
    position: relative;
    width: 453px;
    height: 13px;
    left: 530px;
    top: 146px;
    z-index: 0;
    background-color: #FFF45E;

}
.line-2{
    position: relative;
    top: 170px;
    left: 535px;
    height: 13px;
    width: 420px;
    background-color: #FFF45E; 
} */
</style>
