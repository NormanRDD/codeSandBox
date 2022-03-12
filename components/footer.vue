<template>
  <div class="wrapper">
    <div class="footer-container">
      <div class="footer-wrapper">
        <div class="footer-contacts">
          <div class="contacts-wrapper">
            <div class="contacts">
              <img src="../img/footer/phone.png" alt="" />
              <p class="phone-img">+7 (727) 313 20 50</p>
              <p>+7 (778) 200 20 50</p>
              <p>+7 (777) 078 87 78</p>
              <p>+7 (777) 078 88 33</p>
            </div>
            <div class="contacts-name">
              <p>Ресепшн SmArt.Point</p>
              <p>Ресепшн SmArt.Point</p>
              <p>Аренда сервисных офисов коворкинг-мест</p>
              <p>
                Локаций для съемок, <br />
                размещение рекламы booking5
              </p>
            </div>
          </div>
          <div class="contacts-bot">
            <p class="mail">
              <img src="../img/footer/mail.png" alt="" />
              hello@smartpoint.me
            </p>
            <p class="adress">
              <img src="../img/footer/adress.png" alt="" />
              г. Алматы, ул. Байзакова, 280
            </p>
          </div>
          <div class="vidgets">
            <img class="inst" src="../img/footer/insta.png" alt="" />
            <img class="face" src="../img/footer/face.png" alt="" />
            <div style="display: none" class="border-bot"></div>
          </div>
        </div>
        <div class="nav">
          <ul>
            <li class="about-us"><a href="#about-us">О нас</a></li>
            <li class="out-team"><a href="#our-team">Наша команда</a></li>
            <li class="community"><a href="#community"> Коммьюнити</a></li>
            <li class="gallery"><a href="#gallery">Галлерея</a></li>
            <li class="space"><a href="#space">Пространство</a></li>
            <li class="booking">
              <a href="#bookingg">Онлайн бронирование</a>
            </li>
            <li class="prices"><a href="#prices">Тарифы</a></li>
            <li class="events"><a href="#events">Мероприятия</a></li>
            <li class="news"><a href="#news">Новости</a></li>
            <li class="policy">
              <a href="#policy">Политика конфиденциальности</a>
            </li>
            <li class="rules"><a href="#rules">Правила пространства</a></li>
          </ul>
        </div>
        <div class="logo">
          <div class="pentagon">
            <img src="../img/pentagon.png" alt="" />
          </div>
          <div class="logo-wrapper">
            <img src="../img/logo.svg" alt="" />
          </div>
        </div>
      </div>
    </div>
    <div class="footer">All rights reserved © 2021 smartpoint.me</div>
  </div>
</template>
<script>
import 'assets/css/footer.css'
export default {
  data() {
    return {}
  },
}
</script>
<style scoped>
.footer-container {
  margin: 0 auto;
  margin-bottom: 30px;
  /* padding: 0 auto; */
}

.contacts-bot {
  margin-top: 30px;
  margin-bottom: 30px;
}
.footer-container {
  /* padding-top: 150px; */
}
@media (min-width: 1301px) {
  .contacts-name {
    font-size: 0.9rem;
  }
  .footer-contacts {
    border-right: 1px solid #fff45e;
    margin-right: 20px;
  }
  .footer-contacts {
    /* display: flex; */
  }
  .footer-container {
    width: 1200px;
  }
  .footer-wrapper {
    display: flex;
  }
}
@media (max-width: 650px) {
}
@media (max-width: 1300px) {
  .logo {
    width: 30vw;
  }
  .contacts-wrapper {
    margin: 0 auto;
    width: 61vw;
    margin-bottom: 20px;
  }
  .contacts-bot {
    text-align: center;
    margin: 0 auto;
  }
  .logo {
    margin: 0 auto;
  }
  .vidgets {
    margin: 0 auto;
    width: 21vw;
    margin-top: 15px;
    margin-bottom: 20px;
    text-align: center;
  }
  .nav {
    text-align: center;
    margin: 0 auto;
    width: 22vw;
  }
  .contacts-bot {
    width: 30vw;
  }
  .border-bot {
    border-bottom: 2px solid #fff45e;
    display: block !important;
    margin-bottom: 30px;
    width: 200px;
    margin: 0 auto;
  }
}
@media (max-width: 1000px) {
  .footer-container {
    /* padding-top: 50px; */
  }
  .contacts-bot {
    width: 302px !important;
  }
  .footer-container {
    width: 500px;
  }
  .vidgets {
    width: 210px !important;
  }
  .contacts-wrapper {
    margin: 0 auto;
    width: 321px !important;
    margin-bottom: 32px !important;
    font-size: 10px !important;
  }
  .contacts-bot {
    font-size: 10px;
  }
  .nav {
    width: 150px !important;
  }
}
.footer {
  text-align: center;
  height: 30px;
  padding: 10px;
  color: grey;
  background-color: #fff45e;
}
.pentagon img {
  position: absolute;
  bottom: 5px;
  /* width: 100px; */
}
.contacts img {
  position: relative;
  left: -20%;
  top: 1.5vh;
}
.contacts p {
  padding-bottom: 5px;
}
.contacts-name p {
  padding-bottom: 5px;
}
.wrapper {
  /* margin-top: 50px; */
  /* overflow: hidden; */
  padding-top: 50px;
  /* height: 43vh; */
  color: white;
  background-color: #1d1d1d;
  font-family: sans-serif;
  /* background-color: red; */
}
ul {
  width: 22vw;
}
.inner-wrapper {
  margin: 0 auto;
  width: 1200px;
}
.phone-img {
  display: flex;
}
.contacts-name {
  margin-left: 12px;
  font-weight: 500;
  position: relative;
  color: #9a9a9a;
  top: 2vh;
}
.contacts {
  font-size: 1.2;
}
.contacts-wrapper {
  display: flex;
  flex-grow: 3;
  margin-right: 30px;
}
.nav ul li {
  padding-bottom: 10px;
  flex-grow: 3;
  list-style: none;
}

a {
  text-decoration: none;
  color: white;
}
.mail {
  padding-bottom: 20px;
}
.mail img {
  position: absolute;
  left: -30px;
  /* margin-ri */
}
.adress img {
  position: absolute;
  left: -30px;
}
.logo {
  flex-grow: 1;
  padding-left: 100p;
  position: relative;
}
.logo img {
  width: 287px;
}
.vidgets {
  /* position: relative;
  bottom: 8vh; */
}
.inst {
  margin-right: 50px;
}
</style>
