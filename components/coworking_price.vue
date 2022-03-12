<template>
  <div class="prices-wrapper">
    <div class="coworking-container">
      <h1 class="prices-h1">
        <img src="../img/prices/header.png" alt="" />
        КОВОРКИНГ ПАКЕТЫ
      </h1>
      <div class="prices-box">
        <div class="prices-left">
          <ul class="list">
            <li>
              <div class="right-row">
                <h2 v-if="ip">
                  {{ night.price }}
                </h2>
                <div class="radio-wrapper">
                  <input
                    class="customradio"
                    id="color-green"
                    @change="
                      ;(monthExpVal = false),
                        (proVal = false),
                        (monthVal = false),
                        (weekVal = false),
                        (dayVal = false),
                        (nightVal = true)
                    "
                    checked
                    name="radio"
                    type="radio"
                  />
                  <label for="happy"></label>
                </div>
              </div>

              <p v-if="ip">
                {{ night.number_of_sessions }}
              </p>
            </li>
            <li>
              <div class="right-row">
                <h2 v-if="ip">
                  {{ day.price }}
                </h2>
                <div class="radio-wrapper">
                  <input
                    class="customradio"
                    id="color-green"
                    @change="
                      ;(monthExpVal = false),
                        (proVal = false),
                        (monthVal = false),
                        (weekVal = false),
                        (dayVal = true),
                        (nightVal = false)
                    "
                    name="radio"
                    type="radio"
                  />
                  <label for="happy"></label>
                </div>
              </div>
              <p v-if="ip">
                {{ day.number_of_sessions }}
              </p>
            </li>
            <li>
              <div class="right-row">
                <h2 v-if="ip">
                  {{ week.price }}
                </h2>
                <div class="radio-wrapper">
                  <input
                    class="customradio"
                    id="color-green"
                    @change="
                      ;(monthExpVal = false),
                        (proVal = false),
                        (monthVal = false),
                        (weekVal = true),
                        (dayVal = false),
                        (nightVal = false)
                    "
                    name="radio"
                    type="radio"
                  />
                  <label for="happy"></label>
                </div>
              </div>
              <p v-if="ip">
                {{ week.number_of_sessions }}
              </p>
            </li>
            <li>
              <div class="right-row">
                <h2 v-if="ip">
                  {{ month.price }}
                </h2>
                <div class="radio-wrapper">
                  <input
                    class="customradio"
                    id="color-green"
                    @change="
                      ;(monthExpVal = false),
                        (proVal = false),
                        (monthVal = true),
                        (weekVal = false),
                        (dayVal = false),
                        (nightVal = false)
                    "
                    name="radio"
                    type="radio"
                  />
                  <label for="happy"></label>
                </div>
              </div>
              <p v-if="ip">
                {{ month.number_of_sessions }}
              </p>
            </li>
            <li>
              <div class="right-row">
                <h2 v-if="ip">
                  {{ monthExp.price }}
                </h2>
                <div class="radio-wrapper">
                  <input
                    class="customradio"
                    id="color-green"
                    @change="
                      ;(monthExpVal = true),
                        (proVal = false),
                        (monthVal = false),
                        (weekVal = false),
                        (dayVal = false),
                        (nightVal = false)
                    "
                    name="radio"
                    type="radio"
                  />
                  <label for="happy"></label>
                </div>
              </div>
              <p v-if="ip">
                {{ monthExp.number_of_sessions }}
              </p>
            </li>
            <li>
              <div class="right-row">
                <h2 v-if="ip">
                  {{ pro.price }}
                </h2>
                <div class="radio-wrapper">
                  <input
                    class="customradio"
                    id="color-green"
                    @change="
                      ;(proVal = true),
                        (monthExpVal = false),
                        (monthVal = false),
                        (weekVal = false),
                        (dayVal = false),
                        (nightVal = false)
                    "
                    name="radio"
                    type="radio"
                  />
                  <label for="happy"></label>
                </div>
              </div>
              <p v-if="ip">
                {{ pro.number_of_sessions }}
              </p>
            </li>
          </ul>
        </div>
        <div class="prices-right">
          <div v-if="nightVal" class="night">
            <div class="header">
              <h2 v-if="ip">
                {{ night.price }}
              </h2>
              <h3 v-if="ip">
                Количество посещений: {{ night.number_of_sessions }}
              </h3>
              <br />
            </div>
            <div v-if="ip" class="list-wrapper">
              <ul v-for="el in night.bonus" :key="el.id" class="list">
                <li v-if="ip">
                  <img class="list-image" :src="el.image" alt="" />{{ el.text }}
                </li>
              </ul>
              <button class="list-btn">Купить</button>
            </div>
          </div>

          <div v-if="dayVal" class="day">
            <div class="header">
              <h2 v-if="ip">
                {{ day.price }}
              </h2>
              <h3 v-if="ip">
                Количество посещений: {{ day.number_of_sessions }}
              </h3>
              <br />
            </div>
            <div v-if="ip" class="list-wrapper">
              <ul v-for="el in day.bonus" :key="el.id" class="list">
                <li v-if="ip">
                  <img class="list-image" :src="el.image" />{{ el.text }}
                </li>
              </ul>
              <button class="list-btn">Купить</button>
            </div>
          </div>

          <div v-if="weekVal" class="month">
            <div class="header">
              <h2 v-if="ip">
                {{ week.price }}
              </h2>
              <h3 v-if="ip">
                Количество посещений: {{ week.number_of_sessions }}
              </h3>
              <br />
            </div>
            <div v-if="ip" class="list-wrapper">
              <ul v-for="el in week.bonus" :key="el.id" class="list">
                <li v-if="ip">
                  <img class="list-image" :src="el.image" />{{ el.text }}
                </li>
              </ul>
              <button class="list-btn">Купить</button>
            </div>
          </div>

          <div v-if="monthVal" class="month">
            <div class="header">
              <h2 v-if="ip">
                {{ month.price }}
              </h2>
              <h3 v-if="ip">
                Количество посещений: {{ month.number_of_sessions }}
              </h3>
              <br />
            </div>
            <div v-if="ip" class="list-wrapper">
              <ul v-for="el in month.bonus" :key="el.id" class="list">
                <li v-if="ip">
                  <img class="list-image" :src="el.image" />{{ el.text }}
                </li>
              </ul>
              <button class="list-btn">Купить</button>
            </div>
          </div>

          <div v-if="monthExpVal" class="monthExp">
            <div class="header">
              <h2 v-if="ip">
                {{ monthExp.price }}
              </h2>
              <h3 v-if="ip">
                Количество посещений: {{ monthExp.number_of_sessions }}
              </h3>
              <br />
            </div>
            <div v-if="ip" class="list-wrapper">
              <ul v-for="el in monthExp.bonus" :key="el.id" class="list">
                <li v-if="ip">
                  <img class="list-image" :src="el.image" />{{ el.text }}
                </li>
              </ul>
              <button class="list-btn">Купить</button>
            </div>
          </div>

          <div v-if="proVal" class="pro">
            <div class="header">
              <h2 v-if="ip">
                {{ pro.price }}
              </h2>
              <h3 v-if="ip">
                Количество посещений: {{ pro.number_of_sessions }}
              </h3>
              <br />
            </div>
            <div v-if="ip" class="list-wrapper">
              <ul v-for="el in pro.bonus" :key="el.id" class="list">
                <li v-if="ip">
                  <img class="list-image" :src="el.image" />{{ el.text }}
                </li>
              </ul>
              <button class="list-btn">Купить</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      nightVal: 'true',
      dayVal: '',
      weekVal: '',
      monthVal: '',
      monthExpVal: '',
      proVal: '',
      ip: '',
      // month,
    }
  },
  methods: {
    async fetchSomething() {
      const ip = await this.$axios.$get('https://smartpoint.me/api/coworking')
      this.ip = ip
    },
  },
  computed: {
    night() {
      return this.ip[4]
    },
    day() {
      return this.ip[5]
    },
    week() {
      return this.ip[6]
    },
    month() {
      return this.ip[7]
    },
    monthExp() {
      return this.ip[3]
    },
    pro() {
      return this.ip[2]
    },
  },
  created() {
    // this.exactImg()
    this.fetchSomething()
  },
}
</script>
<style scoped>
@media (min-width: 1240px) {
  .coworking-container {
    width: 1200px;
    margin: 0 auto;
  }
  .list-btn {
    left: 9%;
  }
}
@media (max-width: 1200px) {
  .prices-left {
    display: none;
  }
  .list-btn {
    left: 15%;
  }
  .coworking-container {
    width: 665px;
    margin: 0 auto;
  }
}
@media (max-width: 700px) {
  .coworking-container {
    width: 400px;
    margin: 0 auto;
  }
  .list-btn {
    left: -6%;
  }
}
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
  background-color: #f1f1f1;
}
.prices-box {
  padding: 30px;
}
.prices ul li {
  list-style: none;
}
.prices-right {
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
.prices-left {
  /* display: flex; */
  padding-right: 60px;
  flex-grow: 10;
  background-image: url('../img/prices_background.png');
}
.right-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.prices-left ul li {
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
  border: 1px solid nnight;
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
