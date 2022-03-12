<template>
  <div id="about-us">
    <div class="about-container">
      <div class="header">
        <p class="background-header">О НАС</p>
        <h1 class="inner-header">О НАС</h1>
      </div>
      <div class="about-section">
        <div class="thesis-wrapper">
          <div class="thesis">
            Добро пожаловать в <br />
            пространство разумных <br />
            технологий и креативных <br />
            решений – <br />
            <p class="thesis-header">SmArt.Point!</p>
          </div>
        </div>
        <div class="info-wrapper">
          <p class="info">
            В коворкинге работают более 70 успешных компаний в сфере IT, финтех,
            онлайн-торговли, разработки <br />
            ПО, кибербезопасности, блокчейн, ИТ-образования, онлайн-образования,
            медиа, <br />
            автоматизированной логистики, искусственного интеллекта,
            робототехники, телекоммуникации, digital- <br />
            маркетинга и дизайна, с совокупным количеством сотрудников более 800
            человек
          </p>
          <button class="more">Подробнее</button>
          <div class="info-box">
            <div class="info-top">
              <div class="field">
                <span> 12 000 м² </span>
                <p>Прощадь коворкинга</p>
              </div>
              <div class="places">
                <span> 1 000 </span>
                <p>Рабочих мест</p>
              </div>
            </div>
            <div class="info-bot">
              <div class="speed">
                <span> 500 мб/с </span>
                <p>Интернет Wi-Fi</p>
              </div>
              <div class="acess">
                <span> 24/7 </span>
                <p>Доступ</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.thesis-header {
  font-size: 30px;
  font-weight: 500;
}
.thesis {
  font-size: 22px;
}
.inner-header {
  position: relative;
  font-size: 3.5rem;
  color: #263164;
  font-weight: 600;
  left: 0px;
  padding-top: 60px;
  top: -100px;
  text-align: center;
  font-family: sans-serif;
  padding-bottom: 20px;
}
.background-header {
  overflow: hidden;
  /* padding-top: 60px; */
  text-align: center;
  font-size: 7rem;
  white-space: nowrap;
  font-weight: 700;
  color: transparent;
  -webkit-text-stroke-width: 3px;
  -webkit-text-stroke-color: rgba(52, 52, 52, 0.05);
  position: relative;
  left: 50%;
  top: 119px;
  /* width: 100px; */
  transform: translate(-50%, -50%);
}
.about-container {
  width: 1200px;
  margin-left: auto;
  margin-right: auto;
}
.field {
  flex-grow: 7;
}
.places {
  flex-grow: 20;
}
.speed {
  flex-grow: 7;
}
.acess {
  flex-grow: 20;
}
.info-box {
  font-family: sans-serif;
  position: relative;
  height: 100%;
  width: 100%;
  background-image: url('https://smartpoint.me/_nuxt/img/about-section-bg.6e32c95.png');
}
.info-top span {
  font-weight: 500;
  color: #ffed00;
  font-size: 45px;
}
.info-bot span {
  font-weight: 500;
  color: #ffed00;
  font-size: 45px;
}
.info-top {
  margin-top: 30px;
  margin-bottom: 30px;
  display: flex;
}
.info-bot {
  display: flex;
}
.more-wrapper {
  /* text-align: center; */
  width: 50vw;
  margin-left: 39vw;
}
.more:hover {
  background-color: #354074;
  transition: 0.3s;
}
.more {
  font-family: sans-serif;
  font-weight: 500;
  margin-top: 34px;
  font-size: 16px;
  font-weight: 600;
  padding: 15px 142px 15px 142px;
  border-radius: 5px;
  background-color: #263164;
  color: #fff45e;
}
.about-section {
  justify-content: space-around;
  display: flex;
  padding-bottom: 130px;
}
@media (max-width: 1220px) {
  .about-section {
    flex-direction: column;
  }
  .about-container {
    width: 800px;
  }
}
@media (max-width: 820px) {
  .about-container {
    max-width: 300px;
    width: unset;
  }
  .background-header {
    font-size: 3rem;
  }
  .inner-header {
    font-size: 2rem;
    top: -13px;
  }
}
.about-caption {
  color: #263164;
  font-weight: 700;
  font-size: 20px;
}
.in-about {
  text-align: center;
  position: relative;
  top: -100px;
  font-family: sans-serif;
  font-weight: 700;
  color: #263164;
  font-size: 70px;
}
.back-about {
  padding-top: 30px;
  margin-left: 32vw;
}
.thesis-wrapper {
  width: 310px;
  font-family: sans-serif;
  flex-grow: 5;
  /* margin-left: 200px; */
}
.info-wrapper {
  /* width: 310px; */
  flex-grow: 7;
}
</style>
