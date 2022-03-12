<template>
  <div id="space" class="space-section">
    <div class="space-container">
      <div class="space-header">
        <h1>ПРОСТРАНСТВО</h1>
      </div>
      <div v-if="currentPage == 1" class="wrapper">
        <div class="space-info">
          <div class="space-item space-item-1">
            <div class="space-item-name">
              <h3>Название</h3>
            </div>
            <div class="space-item-header">
              <p>Bon Jovi</p>
              <span
                >Конференц зал отлично подходит для деловых встреч, семинаров
                или конференций.</span
              >
            </div>
          </div>
          <div class="space-item space-item-2">
            <div class="space-item-name">
              <h3>Тип</h3>
            </div>
            <div class="space-item-header">
              <p>Конференц зал</p>
              <span
                >Мебелированные конференц залы с возможностью почасовой аренды,
                прекрасно подходят для проведения деловых встреч и
                переговоров.</span
              >
            </div>
          </div>
          <div class="space-item space-item-3">
            <div class="space-item-name">
              <h3>Площадь</h3>
            </div>
            <div class="space-item-header">
              <p>10м²</p>
              <!-- <span>10 м²</span> -->
            </div>
          </div>

          <div class="space-item space-item-4">
            <div class="space-item-name">
              <h3>Оборудование</h3>
            </div>
            <div class="space-item-header">
              <p>WiFi, экран, HDMI кабель, маркеры</p>
              <!-- <span>WiFi, экран, HDMI кабель, маркеры</span> -->
            </div>
          </div>

          <div class="space-item space-item-5">
            <div class="space-item-name">
              <h3>Вместимость</h3>
            </div>
            <div class="space-item-header">
              <p>
                Максимальная вместительность 5 чел. <br />
                Рекомендуем для встречи 5 чел.
              </p>
              <!-- <span></span> -->
            </div>
          </div>

          <div class="space-item space-item-6">
            <div class="space-item-name">
              <h3>Цена</h3>
            </div>
            <div class="space-item-header">
              <p>4000 KZT/ч.</p>
              <span></span>
            </div>
          </div>
        </div>
        <div class="space-image">
          <img
            class="image"
            src="https://smartpoint.me/media/2021/11/30/1638290709.webp"
            alt=""
          />
        </div>
      </div>
      <div v-if="currentPage == 2" class="wrapper">
        <div class="space-info">
          <div class="space-item space-item-1">
            <div class="space-item-name">
              <h3>Название</h3>
            </div>
            <div class="space-item-header">
              <p>A-Studio</p>
              <span
                >Конференц зал отлично подходит для деловых встреч, семинаров
                или конференций.</span
              >
            </div>
          </div>
          <div class="space-item space-item-2">
            <div class="space-item-name">
              <h3>Тип</h3>
            </div>
            <div class="space-item-header">
              <p>Конференц зал</p>
              <span
                >Мебелированные конференц залы с возможностью почасовой аренды,
                прекрасно подходят для проведения деловых встреч и
                переговоров.</span
              >
            </div>
          </div>
          <div class="space-item space-item-3">
            <div class="space-item-name">
              <h3>Площадь</h3>
            </div>
            <div class="space-item-header">
              <p>52м²</p>
              <!-- <span>10 м²</span> -->
            </div>
          </div>

          <div class="space-item space-item-4">
            <div class="space-item-name">
              <h3>Оборудование</h3>
            </div>
            <div class="space-item-header">
              <p>Проектор, интерактивная доска</p>
              <!-- <span>WiFi, экран, HDMI кабель, маркеры</span> -->
            </div>
          </div>

          <div class="space-item space-item-5">
            <div class="space-item-name">
              <h3>Вместимость</h3>
            </div>
            <div class="space-item-header">
              <p>
                Максимальная вместительность 30 чел. <br />
                Рекомендуем для встречи 30 чел.
              </p>
              <!-- <span></span> -->
            </div>
          </div>

          <div class="space-item space-item-6">
            <div class="space-item-name">
              <h3>Цена</h3>
            </div>
            <div class="space-item-header">
              <p>12000 KZT/ч.</p>
              <span></span>
            </div>
          </div>
        </div>
        <div class="space-image">
          <img
            class="image"
            src="https://smartpoint.me/media/2021/11/30/1638290787.webp"
            alt=""
          />
        </div>
      </div>
      <div v-if="currentPage == 3" class="wrapper">
        <div class="space-info">
          <div class="space-item space-item-1">
            <div class="space-item-name">
              <h3>Название</h3>
            </div>
            <div class="space-item-header">
              <p>Patio</p>
              <span
                >Отлично подходит для деловых встреч, семинаров или
                конференций.</span
              >
            </div>
          </div>
          <div class="space-item space-item-2">
            <div class="space-item-name">
              <h3>Тип</h3>
            </div>
            <div class="space-item-header">
              <p>Конференц зал</p>
              <span
                >Мебелированные конференц залы с возможностью почасовой аренды,
                прекрасно подходят для проведения деловых встреч и
                переговоров.</span
              >
            </div>
          </div>
          <div class="space-item space-item-3">
            <div class="space-item-name">
              <h3>Площадь</h3>
            </div>
            <div class="space-item-header">
              <p>100м²</p>
              <!-- <span>10 м²</span> -->
            </div>
          </div>

          <div class="space-item space-item-4">
            <div class="space-item-name">
              <h3>Оборудование</h3>
            </div>
            <div class="space-item-header">
              <p>Проектор, экран, колонки, радиомикрофоны</p>
              <!-- <span>WiFi, экран, HDMI кабель, маркеры</span> -->
            </div>
          </div>

          <div class="space-item space-item-5">
            <div class="space-item-name">
              <h3>Вместимость</h3>
            </div>
            <div class="space-item-header">
              <p>
                Максимальная вместительность 50 чел. <br />
                Рекомендуем для встречи 50 чел.
              </p>
              <!-- <span></span> -->
            </div>
          </div>

          <div class="space-item space-item-6">
            <div class="space-item-name">
              <h3>Цена</h3>
            </div>
            <div class="space-item-header">
              <p>15000 KZT/ч.</p>
              <span></span>
            </div>
          </div>
        </div>
        <div class="space-image">
          <img
            class="image"
            src="https://smartpoint.me/media/2021/11/30/1638290642.webp"
            alt=""
          />
        </div>
      </div>
      <div v-if="currentPage == 4" class="wrapper">
        <div class="space-info">
          <div class="space-item space-item-1">
            <div class="space-item-name">
              <h3>Название</h3>
            </div>
            <div class="space-item-header">
              <p>Deep Purple</p>
              <span
                >Конференц зал отлично подходит для деловых встреч, семинаров
                или конференций.</span
              >
            </div>
          </div>
          <div class="space-item space-item-2">
            <div class="space-item-name">
              <h3>Тип</h3>
            </div>
            <div class="space-item-header">
              <p>Конференц зал</p>
              <span
                >Мебелированные конференц залы с возможностью почасовой аренды,
                прекрасно подходят для проведения деловых встреч и
                переговоров.</span
              >
            </div>
          </div>
          <div class="space-item space-item-3">
            <div class="space-item-name">
              <h3>Площадь</h3>
            </div>
            <div class="space-item-header">
              <p>52м²</p>
              <!-- <span>10 м²</span> -->
            </div>
          </div>

          <div class="space-item space-item-4">
            <div class="space-item-name">
              <h3>Оборудование</h3>
            </div>
            <div class="space-item-header">
              <p>Проектор, интерактивная доска</p>
              <!-- <span>WiFi, экран, HDMI кабель, маркеры</span> -->
            </div>
          </div>

          <div class="space-item space-item-5">
            <div class="space-item-name">
              <h3>Вместимость</h3>
            </div>
            <div class="space-item-header">
              <p>
                Максимальная вместительность 35 чел. <br />
                Рекомендуем для встречи 20 чел.
              </p>
              <!-- <span></span> -->
            </div>
          </div>

          <div class="space-item space-item-6">
            <div class="space-item-name">
              <h3>Цена</h3>
            </div>
            <div class="space-item-header">
              <p>10 000 KZT/ч.</p>
              <span></span>
            </div>
          </div>
        </div>
        <div class="space-image">
          <img
            class="image"
            src="https://smartpoint.me/media/2021/11/30/1638290832.webp"
            alt=""
          />
        </div>
      </div>
      <div v-if="currentPage == 5" class="wrapper">
        <div class="space-info">
          <div class="space-item space-item-1">
            <div class="space-item-name">
              <h3>Название</h3>
            </div>
            <div class="space-item-header">
              <p>Gorillaz</p>
              <span
                >Конференц зал отлично подходит для деловых встреч, семинаров
                или конференций.</span
              >
            </div>
          </div>
          <div class="space-item space-item-2">
            <div class="space-item-name">
              <h3>Тип</h3>
            </div>
            <div class="space-item-header">
              <p>Конференц зал</p>
              <span
                >Мебелированные конференц залы с возможностью почасовой аренды,
                прекрасно подходят для проведения деловых встреч и
                переговоров.</span
              >
            </div>
          </div>
          <div class="space-item space-item-3">
            <div class="space-item-name">
              <h3>Площадь</h3>
            </div>
            <div class="space-item-header">
              <p>85м²</p>
              <!-- <span>10 м²</span> -->
            </div>
          </div>

          <div class="space-item space-item-4">
            <div class="space-item-name">
              <h3>Оборудование</h3>
            </div>
            <div class="space-item-header">
              <p>Экран, интерактивная доска</p>
              <!-- <span>WiFi, экран, HDMI кабель, маркеры</span> -->
            </div>
          </div>

          <div class="space-item space-item-5">
            <div class="space-item-name">
              <h3>Вместимость</h3>
            </div>
            <div class="space-item-header">
              <p>
                Максимальная вместительность 50 чел. <br />
                Рекомендуем для встречи 40 чел.
              </p>
              <!-- <span></span> -->
            </div>
          </div>

          <div class="space-item space-item-6">
            <div class="space-item-name">
              <h3>Цена</h3>
            </div>
            <div class="space-item-header">
              <p>12 000 KZT/ч.</p>
              <span></span>
            </div>
          </div>
        </div>
        <div class="space-image">
          <img
            class="image"
            src="https://smartpoint.me/media/2021/11/30/1638290594.webp"
            alt=""
          />
        </div>
      </div>
      <div v-if="currentPage == 6" class="wrapper">
        <div class="space-info">
          <div class="space-item space-item-1">
            <div class="space-item-name">
              <h3>Название</h3>
            </div>
            <div class="space-item-header">
              <p>Green Day</p>
              <span
                >Конференц зал отлично подходит для деловых встреч, семинаров
                или конференций.</span
              >
            </div>
          </div>
          <div class="space-item space-item-2">
            <div class="space-item-name">
              <h3>Тип</h3>
            </div>
            <div class="space-item-header">
              <p>Конференц зал</p>
              <span
                >Мебелированные конференц залы с возможностью почасовой аренды,
                прекрасно подходят для проведения деловых встреч и
                переговоров.</span
              >
            </div>
          </div>
          <div class="space-item space-item-3">
            <div class="space-item-name">
              <h3>Площадь</h3>
            </div>
            <div class="space-item-header">
              <p>25м²</p>
              <!-- <span>10 м²</span> -->
            </div>
          </div>

          <div class="space-item space-item-4">
            <div class="space-item-name">
              <h3>Оборудование</h3>
            </div>
            <div class="space-item-header">
              <p>Проектор, интерактивная доска</p>
              <!-- <span>WiFi, экран, HDMI кабель, маркеры</span> -->
            </div>
          </div>

          <div class="space-item space-item-5">
            <div class="space-item-name">
              <h3>Вместимость</h3>
            </div>
            <div class="space-item-header">
              <p>
                Максимальная вместительность 16 чел. <br />
                Рекомендуем для встречи 14 чел.
              </p>
              <!-- <span></span> -->
            </div>
          </div>

          <div class="space-item space-item-6">
            <div class="space-item-name">
              <h3>Цена</h3>
            </div>
            <div class="space-item-header">
              <p>8 000 KZT/ч.</p>
              <span></span>
            </div>
          </div>
        </div>
        <div class="space-image">
          <img
            class="image"
            src="https://smartpoint.me/media/2021/11/30/1638290620.webp"
            alt=""
          />
        </div>
      </div>
      <div v-if="currentPage == 7" class="wrapper">
        <div class="space-info">
          <div class="space-item space-item-1">
            <div class="space-item-name">
              <h3>Название</h3>
            </div>
            <div class="space-item-header">
              <p>Viktor Tsoi</p>
              <span
                >Конференц зал отлично подходит для деловых встреч, семинаров
                или конференций.</span
              >
            </div>
          </div>
          <div class="space-item space-item-2">
            <div class="space-item-name">
              <h3>Тип</h3>
            </div>
            <div class="space-item-header">
              <p>Конференц зал</p>
              <span
                >Мебелированные конференц залы с возможностью почасовой аренды,
                прекрасно подходят для проведения деловых встреч и
                переговоров.</span
              >
            </div>
          </div>
          <div class="space-item space-item-3">
            <div class="space-item-name">
              <h3>Площадь</h3>
            </div>
            <div class="space-item-header">
              <p>31м²</p>
              <!-- <span>10 м²</span> -->
            </div>
          </div>

          <div class="space-item space-item-4">
            <div class="space-item-name">
              <h3>Оборудование</h3>
            </div>
            <div class="space-item-header">
              <p>Проектор, интерактивная доска</p>
              <!-- <span>WiFi, экран, HDMI кабель, маркеры</span> -->
            </div>
          </div>

          <div class="space-item space-item-5">
            <div class="space-item-name">
              <h3>Вместимость</h3>
            </div>
            <div class="space-item-header">
              <p>
                Максимальная вместительность 10 чел. <br />
                Рекомендуем для встречи 10 чел.
              </p>
              <!-- <span></span> -->
            </div>
          </div>

          <div class="space-item space-item-6">
            <div class="space-item-name">
              <h3>Цена</h3>
            </div>
            <div class="space-item-header">
              <p>10 000 KZT/ч.</p>
              <span></span>
            </div>
          </div>
        </div>
        <div class="space-image">
          <img
            class="image"
            src="https://smartpoint.me/media/2021/11/30/1638290768.webp"
            alt=""
          />
        </div>
      </div>
      <div v-if="currentPage == 8" class="wrapper">
        <div class="space-info">
          <div class="space-item space-item-1">
            <div class="space-item-name">
              <h3>Название</h3>
            </div>
            <div class="space-item-header">
              <p>Freedom</p>
              <span
                >Конференц зал отлично подходит для деловых встреч, семинаров
                или конференций.</span
              >
            </div>
          </div>
          <div class="space-item space-item-2">
            <div class="space-item-name">
              <h3>Тип</h3>
            </div>
            <div class="space-item-header">
              <p>Конференц зал</p>
              <span
                >Мебелированные конференц залы с возможностью почасовой аренды,
                прекрасно подходят для проведения деловых встреч и
                переговоров.</span
              >
            </div>
          </div>
          <div class="space-item space-item-3">
            <div class="space-item-name">
              <h3>Площадь</h3>
            </div>
            <div class="space-item-header">
              <p>171м²</p>
              <!-- <span>10 м²</span> -->
            </div>
          </div>

          <div class="space-item space-item-4">
            <div class="space-item-name">
              <h3>Оборудование</h3>
            </div>
            <div class="space-item-header">
              <p>Проектор, экран, колонки, радиомикрофоны</p>
              <!-- <span>WiFi, экран, HDMI кабель, маркеры</span> -->
            </div>
          </div>

          <div class="space-item space-item-5">
            <div class="space-item-name">
              <h3>Вместимость</h3>
            </div>
            <div class="space-item-header">
              <p>
                Максимальная вместительность 100 чел. <br />
                Рекомендуем для встречи 70 чел.
              </p>
              <!-- <span></span> -->
            </div>
          </div>

          <div class="space-item space-item-6">
            <div class="space-item-name">
              <h3>Цена</h3>
            </div>
            <div class="space-item-header">
              <p>18 000 KZT/ч.</p>
              <span></span>
            </div>
          </div>
        </div>
        <div class="space-image">
          <img
            class="image"
            src="https://smartpoint.me/media/2021/11/30/1638290727.webp"
            alt=""
          />
        </div>
      </div>
      <div v-if="currentPage == 9" class="wrapper">
        <div class="space-info">
          <div class="space-item space-item-1">
            <div class="space-item-name">
              <h3>Название</h3>
            </div>
            <div class="space-item-header">
              <p>Genesis</p>
              <span
                >Конференц зал отлично подходит для деловых встреч, семинаров
                или конференций.</span
              >
            </div>
          </div>
          <div class="space-item space-item-2">
            <div class="space-item-name">
              <h3>Тип</h3>
            </div>
            <div class="space-item-header">
              <p>Конференц зал</p>
              <span
                >Мебелированные конференц залы с возможностью почасовой аренды,
                прекрасно подходят для проведения деловых встреч и
                переговоров.</span
              >
            </div>
          </div>
          <div class="space-item space-item-3">
            <div class="space-item-name">
              <h3>Площадь</h3>
            </div>
            <div class="space-item-header">
              <p>10м²</p>
              <!-- <span>10 м²</span> -->
            </div>
          </div>

          <div class="space-item space-item-4">
            <div class="space-item-name">
              <h3>Оборудование</h3>
            </div>
            <div class="space-item-header">
              <p>WiFi, экран, HDMI кабель, маркеры</p>
              <!-- <span>WiFi, экран, HDMI кабель, маркеры</span> -->
            </div>
          </div>

          <div class="space-item space-item-5">
            <div class="space-item-name">
              <h3>Вместимость</h3>
            </div>
            <div class="space-item-header">
              <p>
                Максимальная вместительность 5 чел. <br />
                Рекомендуем для встречи 5 чел.
              </p>
              <!-- <span></span> -->
            </div>
          </div>

          <div class="space-item space-item-6">
            <div class="space-item-name">
              <h3>Цена</h3>
            </div>
            <div class="space-item-header">
              <p>4 000 KZT/ч.</p>
              <span></span>
            </div>
          </div>
        </div>
        <div class="space-image">
          <img
            class="image"
            src="https://smartpoint.me/media/2021/11/30/1638290668.webp"
            alt=""
          />
        </div>
      </div>
      <div v-if="currentPage == 10" class="wrapper">
        <div class="space-info">
          <div class="space-item space-item-1">
            <div class="space-item-name">
              <h3>Название</h3>
            </div>
            <div class="space-item-header">
              <p>Aerosmith</p>
              <span
                >Конференц зал отлично подходит для деловых встреч, семинаров
                или конференций.</span
              >
            </div>
          </div>
          <div class="space-item space-item-2">
            <div class="space-item-name">
              <h3>Тип</h3>
            </div>
            <div class="space-item-header">
              <p>Конференц зал</p>
              <span
                >Мебелированные конференц залы с возможностью почасовой аренды,
                прекрасно подходят для проведения деловых встреч и
                переговоров.</span
              >
            </div>
          </div>
          <div class="space-item space-item-3">
            <div class="space-item-name">
              <h3>Площадь</h3>
            </div>
            <div class="space-item-header">
              <p>10м²</p>
              <!-- <span>10 м²</span> -->
            </div>
          </div>

          <div class="space-item space-item-4">
            <div class="space-item-name">
              <h3>Оборудование</h3>
            </div>
            <div class="space-item-header">
              <p>WiFi, экран, HDMI кабель, маркеры</p>
              <!-- <span>WiFi, экран, HDMI кабель, маркеры</span> -->
            </div>
          </div>

          <div class="space-item space-item-5">
            <div class="space-item-name">
              <h3>Вместимость</h3>
            </div>
            <div class="space-item-header">
              <p>
                Максимальная вместительность 5 чел. <br />
                Рекомендуем для встречи 5 чел.
              </p>
              <!-- <span></span> -->
            </div>
          </div>

          <div class="space-item space-item-6">
            <div class="space-item-name">
              <h3>Цена</h3>
            </div>
            <div class="space-item-header">
              <p>4 000 KZT/ч.</p>
              <span></span>
            </div>
          </div>
        </div>
        <div class="space-image">
          <img
            class="image"
            src="https://smartpoint.me/media/2021/11/30/1638290689.webp"
            alt=""
          />
        </div>
      </div>
      <div v-if="currentPage == 11" class="wrapper">
        <div class="space-info">
          <div class="space-item space-item-1">
            <div class="space-item-name">
              <h3>Название</h3>
            </div>
            <div class="space-item-header">
              <p>Smart Space</p>
              <span
                >Конференц зал отлично подходит для деловых встреч, семинаров
                или конференций.</span
              >
            </div>
          </div>
          <div class="space-item space-item-2">
            <div class="space-item-name">
              <h3>Тип</h3>
            </div>
            <div class="space-item-header">
              <p>Конференц зал</p>
              <span
                >Мебелированные конференц залы с возможностью почасовой аренды,
                прекрасно подходят для проведения деловых встреч и
                переговоров.</span
              >
            </div>
          </div>
          <div class="space-item space-item-3">
            <div class="space-item-name">
              <h3>Площадь</h3>
            </div>
            <div class="space-item-header">
              <p>349м²</p>
              <!-- <span>10 м²</span> -->
            </div>
          </div>

          <div class="space-item space-item-4">
            <div class="space-item-name">
              <h3>Оборудование</h3>
            </div>
            <div class="space-item-header">
              <p>Проектор, экран, колонки, радиомикрофоны</p>
              <!-- <span>WiFi, экран, HDMI кабель, маркеры</span> -->
            </div>
          </div>

          <div class="space-item space-item-5">
            <div class="space-item-name">
              <h3>Вместимость</h3>
            </div>
            <div class="space-item-header">
              <p>
                Максимальная вместительность 150 чел. <br />
                Рекомендуем для встречи 120 чел.
              </p>
              <!-- <span></span> -->
            </div>
          </div>

          <div class="space-item space-item-6">
            <div class="space-item-name">
              <h3>Цена</h3>
            </div>
            <div class="space-item-header">
              <p>25 000 KZT/ч.</p>
              <span></span>
            </div>
          </div>
        </div>
        <div class="space-image">
          <img
            class="image"
            src="https://smartpoint.me/media/2021/11/30/1638290745.webp"
            alt=""
          />
        </div>
      </div>
      <div v-if="currentPage == 12" class="wrapper">
        <div class="space-info">
          <div class="space-item space-item-1">
            <div class="space-item-name">
              <h3>Название</h3>
            </div>
            <div class="space-item-header">
              <p>Aphitheatre</p>
              <span
                >Конференц зал отлично подходит для деловых встреч, семинаров
                или конференций.</span
              >
            </div>
          </div>
          <div class="space-item space-item-2">
            <div class="space-item-name">
              <h3>Тип</h3>
            </div>
            <div class="space-item-header">
              <p>Конференц зал</p>
              <span
                >Мебелированные конференц залы с возможностью почасовой аренды,
                прекрасно подходят для проведения деловых встреч и
                переговоров.</span
              >
            </div>
          </div>
          <div class="space-item space-item-3">
            <div class="space-item-name">
              <h3>Площадь</h3>
            </div>
            <div class="space-item-header">
              <p>303м²</p>
              <!-- <span>10 м²</span> -->
            </div>
          </div>

          <div class="space-item space-item-4">
            <div class="space-item-name">
              <h3>Оборудование</h3>
            </div>
            <div class="space-item-header">
              <p>Проектор, экран, колонки, радиомикрофоны</p>
              <!-- <span>WiFi, экран, HDMI кабель, маркеры</span> -->
            </div>
          </div>

          <div class="space-item space-item-5">
            <div class="space-item-name">
              <h3>Вместимость</h3>
            </div>
            <div class="space-item-header">
              <p>
                Максимальная вместительность 120 чел. <br />
                Рекомендуем для встречи 100 чел.
              </p>
              <!-- <span></span> -->
            </div>
          </div>

          <div class="space-item space-item-6">
            <div class="space-item-name">
              <h3>Цена</h3>
            </div>
            <div class="space-item-header">
              <p>18 000 KZT/ч.</p>
              <span></span>
            </div>
          </div>
        </div>
        <div class="space-image">
          <img
            class="image"
            src="https://smartpoint.me/media/2021/11/30/1638290812.webp"
            alt=""
          />
        </div>
      </div>
      <div class="page-nav">
        <img
          @click="prev"
          class="arrow-1"
          src="../img/space/arrow.png"
          alt=""
        />
        <p class="current-page">{{ currentPage }} / {{ pages }}</p>
        <img
          @click="next"
          class="arrow-2"
          src="../img/space/arrow.png"
          alt=""
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      pages: 12,
      currentPage: 1,
    }
  },
  methods: {
    next() {
      if (this.currentPage < this.pages) {
        this.currentPage++
      } else {
        this.currentPage
      }
    },
    prev() {
      if (this.currentPage > 1) {
        this.currentPage--
      } else {
        this.currentPage
      }
    },
  },
}
</script>
<style scoped>
.space-container {
  margin: 0 auto;
}
@media(max-width:870px){
    .space-item{
        display: block !important;
        width: 500px !important;
    }
    .space-item:not(:last-child){
        padding-bottom: 30px !important;
    }
    .space-container{
        width: 500px !important;
    }
    .arrow-1{
        left: 48% !important;
    }
    .arrow-2{
        left: 60% !important;
    }
}
@media (min-width: 1201px) {
  .space-container {
    width: 1200px;
  }
  .wrapper {
    margin-top: 45px;
    justify-content: space-around;
    display: flex;
    margin-left: 60px;
    margin-right: 51px;
  }
}
@media (max-width: 1200px) {
  .space-container {
    width: 700px;
  }
  .space-image{
      text-align: center;
  }
}
.current-page {
  position: relative;
  right: 75px;
  color: #fff45e;
  font-size: 30px;
  font-weight: 500;
  /* margin-right:20px ; */
}
.arrow-1 {
  transform: rotate(180deg);
  position: absolute;
  left: 50%;
}
.arrow-2 {
  position: absolute;
  left: 55%;
}
.page-nav {
  display: flex;
  justify-content: center;
  margin-top: 30px;
}
.image {
  width: 488px;
  border-radius: 10px;
}
.space-header {
  background-image: url('../img/space/space-background.png');
  background-size: cover;
  color: aliceblue;
  text-align: center;
  height: 150px;
  align-items: center;
  widows: 50%;
}
.space-header h1 {
  font-size: 60px;
  padding-top: 50px;
}
.space-section {
  color: aliceblue;
  font-family: sans-serif;
  padding: 120px 0;
  background-color: #1d1d1d;
}

.wrapper::after {
  transition: 0.5s;
}
.space-item {
  /* justify-content: ; */
  display: flex;
  margin-bottom: 18px;
  width: 700px;
}
.space-item-header {
  /* display: flex; */
  font-size: 16spx;
  font-weight: 400;
  color: hsla(0, 0%, 100%, 0.6);
  line-height: 19px;
}
.space-item-header p {
  color: aliceblue;
  margin-bottom: 10px;
}
.space-item h3 {
  margin-right: 40px;
}
.space-item-name {
  font-size: 20px;
  font-weight: 600;
  color: #fff45e;
  min-width: 212px;
  flex-wrap: nowrap;
  margin-right: 40px;
}
</style>
