<template>
  <div id="prices" class="prices-wrapper">
    <div class="prices-container">
      <h1 class="prices-h1">
        <img src="../img/prices/header.png" alt="" />
        СЕРВИСНЫЕ ОФИСЫ
      </h1>
      <div class="prices-box">
        <div class="prices-left">
          <div class="hooper-wrapper">
            <div v-if="one" class="first">
              <div class="header">
                <h2 v-if="ip">
                  {{ first.price }}
                </h2>
                <h3 v-if="ip">
                  Количество посещений: {{ first.number_of_sessions }}
                </h3>
                <br />
                <h3 v-if="ip">
                  {{ first.working_places }}
                </h3>
              </div>
              <div v-if="ip" class="list-wrapper">
                <ul v-for="el in first.bonus" :key="el.id" class="list">
                  <li v-if="ip">
                    <img class="list-image" :src="el.image" alt="" />{{
                      el.text
                    }}
                  </li>
                </ul>
                <button class="list-btn">Купить</button>
              </div>
            </div>
            <div v-if="two" class="second">
              <div class="header">
                <h2 v-if="ip">
                  {{ second.price }}
                </h2>
                <h3 v-if="ip">
                  Количество посещений: {{ second.number_of_sessions }}
                </h3>
                <br />
                <h3 v-if="ip">
                  {{ second.working_places }}
                </h3>
              </div>
              <div v-if="ip" class="list-wrapper">
                <ul v-for="el in second.bonus" :key="el.id" class="list">
                  <li v-if="ip">
                    <img class="list-image" :src="el.image" />{{ el.text }}
                  </li>
                </ul>
                <button class="list-btn">Купить</button>
              </div>
            </div>
            <div v-if="three" class="three">
              <div class="header">
                <h2 v-if="ip">
                  {{ third.price }}
                </h2>
                <h3 v-if="ip">
                  Количество посещений: {{ third.number_of_sessions }}
                </h3>
                <br />
                <h3 v-if="ip">
                  {{ third.working_places }}
                </h3>
              </div>
              <div v-if="ip" class="list-wrapper">
                <ul v-for="el in third.bonus" :key="el.id" class="list">
                  <li v-if="ip">
                    <img class="list-image" :src="el.image" />{{ el.text }}
                  </li>
                </ul>
                <button class="list-btn">Купить</button>
              </div>
            </div>
          </div>
          <div class="own-hooper">
            <hooper
              ref="hooper"
              v-if="ip"
              :centerMode="true"
              style="height: 100%"
            >
              <slide v-for="item in ip_mobile" :key="item.id">
                <div class="first">
                  <div class="header">
                    <h2 v-text="item.price"></h2>
                    <h3>Количество посещений: {{ item.number_of_sessions }}</h3>
                    <br />
                    <h3 v-text="item.working_places"></h3>
                  </div>
                  <div class="list-wrapper">
                    <ul v-for="el in item.bonus" :key="el.id" class="list">
                      <li v-if="ip">
                        <img class="list-image" :src="el.image" alt="" />{{
                          el.text
                        }}
                      </li>
                    </ul>
                    <button class="list-btn">Купить</button>
                  </div>
                </div>
              </slide>
            </hooper>
          </div>
        </div>
        <div class="prices-right">
          <ul class="list">
            <li>
              <div class="right-row">
                <h3>150 000 тг</h3>
                <div class="radio-wrapper">
                  <input
                    class="customradio"
                    id="color-green"
                    @click=";(one = true), (two = false), (three = false)"
                    checked
                    name="radio"
                    type="radio"
                  />
                  <label for="happy"></label>
                </div>
              </div>

              3 рабочих места
            </li>
            <li>
              <div class="right-row">
                <h3>250 000 тг</h3>
                <div class="radio-wrapper">
                  <input
                    class="customradio"
                    id="color-green"
                    @click=";(two = true), (one = false), (three = false)"
                    name="radio"
                    type="radio"
                  />
                  <label for="happy"></label>
                </div>
              </div>
              6 рабочих мест
            </li>
            <li>
              <div class="right-row">
                <h3>450 000 тг</h3>
                <div class="radio-wrapper">
                  <input
                    class="customradio"
                    id="color-green"
                    @click=";(three = true), (two = false), (one = false)"
                    name="radio"
                    type="radio"
                  />
                  <label for="happy"></label>
                </div>
              </div>

              10 рабочих мест
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { Hooper, Slide } from 'hooper'
// import 'assets/css/prices-hooper.css'
// import 'assets/css/hooper.css'
export default {
  components: {
    Hooper,
    Slide,
  },
  data() {
    return {
      // hooperActive: false,
      width: null,
      one: 'true',
      two: '',
      three: '',
      ip: '',
      ip_mobile: [],
    }
  },
  methods: {
    // updateWidth() {
    //   this.width = window.innerWidth
    //   if (this.width <= 1200) {

    //     this.hooperActive = true
    //   }
    //   else {
    //     return
    //   }
    // },
    async fetchSomething() {
      const ip = await this.$axios.$get('https://smartpoint.me/api/coworking')
      this.ip = ip
      this.ip_mobile.push(ip[8])
      this.ip_mobile.push(ip[0])
      this.ip_mobile.push(ip[1])
      // setTimeout(() => {
      //   this.$refs.hooper.updateWidth();
      // }, 0);
    },
  },
  computed: {
    first() {
      return this.ip[8]
    },
    second() {
      return this.ip[0]
    },
    third() {
      return this.ip[1]
    },
  },
  created() {
    // this.exactImg()
    this.fetchSomething()
  },
  // mounted(){
  //    window.addEventListener('resize', this.updateWidth);
  //   this.updateWidth();
  // }
}
</script>
<style scoped>
.prices-container {
  width: 1200px;
  margin: 0 auto;
}
@media (min-width: 1200px) {
  .list-btn {
    left: 12%;
  }
  .own-hooper {
    display: none;
  }
}
@media (max-width: 1240px) {
  .prices-right {
    display: none;
  }
  .prices-container {
    width: 700px;
    margin: 0 auto;
  }
  .list-btn {
    left: 16%;
  }
  .hooper-wrapper {
    display: none;
  }
}
@media (max-width: 740px) {
  ul li:not(:last-child) {
    /* margin-right: 130px; */
  }
  .prices-left {
    width: 150px;
  }
  .prices-container {
    width: 400px;
    margin: 0 auto;
  }
  .list-btn {
    left: -6%;
  }
}
/* @media (max-width: 400px) {
        .prices-container {
            width: 400px;
            margin: 0 auto;
        }
        } */
.prices-h1 {
  color: #263164;
  font-size: 50px;
}
.prices-h1 img {
  position: relative;
  width: 82%;
  bottom: -85px;
}
.list-image {
  margin-right: 5px;
}
h3 {
  margin-bottom: 30px;
}
.list li {
  margin-bottom: 20px;
}
.list-btn {
  width: 285px;
  height: 50px;
  background: #263164;
  box-shadow: 0 10px 20px rgb(38 49 100 / 15%);
  border-radius: 5px;
  font-size: 20px;
  font-weight: 500;
  color: #fff45e;
  transition: all 0.1s;
  position: relative;
}
.prices-wrapper {
  font-family: sans-serif;
  padding: 30px;
}
.prices-box {
  padding: 30px;
}
ul li {
  list-style: none;
}
.prices-left {
  margin-right: 30px;
  flex-grow: 3;
  width: 250px;
  /* padding-left: 150px; */
  background: #fff;
  box-shadow: 0 10px 20px rgb(138 149 158 / 15%);
  border-radius: 5px;
  padding: 50px 78px 60px;
}
.header {
  text-align: center;
}

/* ///////////////////right///////////// */
.prices-right {
  /* display: flex; */
  flex-grow: 10;
  background-image: url('../img/prices_background.png');
}
.right-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.prices-right ul li {
  padding-bottom: 10px;
  border-bottom: 1px solid black;
  list-style: none;
}
.radio-wrapper {
  padding: 5px;
  border-radius: 50%;
  border: 1px solid black;
  width: 24.5px;
  height: 24.5px;
  margin-top: 14px;
}
.customradio {
  position: absolute;
  opacity: 0;
  z-index: 1;
  height: 27px;
  width: 27px;
}
.customradio + label::before {
  /* content: ''; */
  /* display: inline-block; */
  width: 25px;
  height: 25px;
  /* flex-shrink: 0; */
  /* flex-grow: 0; */
  /* background-color: #fff45e; */
  /* border: 3px solid red; */
  border-radius: 50%;
  /* margin-right: 0.5em; */
  /* background-repeat: no-repeat; */
  /* background-position: center center; */
  /* background-size: 50% 50%; */
}
.customradio:checked + label::before {
  content: '';
  display: block;
  width: 25px;
  height: 25-x;
  border: 1px solid none;
  background-color: #fff45e;
  border-radius: 50%;
  /* background-size: 50% 10%; */
}
.prices-wrapper h1 {
  text-align: center;
}
.prices-box {
  justify-content: space-around;
  /* text-align: center; */
  display: flex;
}
</style>
