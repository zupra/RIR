<template lang="pug">

.Cities.py-5
  .wrap
    h2.text_x5 Города-участники
    p.subText Умный город — это целая линейка системных решений для городов разного размера и специфики их развития. Сегодня цифровая платформа «Умный город» развёрнута на территории 12 городов:


  .m-4
    client-only
      swiper(
        :options="swiperOption"
      )
        swiper-slide(
          v-for="It in slides"
          :key="It.id"
        )

          .city_item.center
            img.city_logo(
              :src="require(`~/static/icon/logo_of_сities/${It.id}.png`)"
            )
            .H.text_x1 {{It.city}}
            .H.my-3 {{It.region}}
            a.btn(
              :href="It.site"
              target="_blank"
            ) Подробнее
      .swiper-button-prev(
        slot="button-prev"
      ) &nbsp;
      .swiper-button-next(
        slot="button-next"
      ) &nbsp;

</template>

<script>
// import 'swiper/css/swiper.css'

const DATA = [
  {
    id: 1,
    city: 'Глазов',
    site: 'https://glazov.rosatom.city/',
    region: 'Удмуртская Республика'
  },
  {
    id: 2,
    city: 'Новоуральск',
    site: 'https://novouralsk.rosatom.city/',
    region: 'Свердловская область'
  },
  {
    id: 3,
    city: 'Саров',
    site: 'https://smartsarov.ru/',
    region: 'Нижегородская область'
  },
  {
    id: 4,
    city: 'Железногорск',
    site: 'https://zhel.rosatom.city/',
    region: 'Красноярский край'
  },

  {
    id: 5,
    city: 'Заречный',
    site: 'https://zarechny.rosatom.city/',
    region: 'Свердловская область'
  },
  {
    id: 6,
    city: 'Заречный',
    site: 'https://zarechnyzato.rosatom.city/',
    region: 'Пензенская область'
  },
  {
    id: 7,
    city: 'Лесной',
    site: 'https://lesnoy.rosatom.city/',
    region: 'Свердловская область'
  },
  {
    id: 8,
    city: 'Озёрск',
    site: 'https://ozersk.rosatom.city/',
    region: 'Челябинская область'
  },
  {
    id: 9,
    city: 'Северск',
    site: 'https://seversk.rosatom.city/',
    region: 'Томская область'
  },
  {
    id: 10,
    city: 'Снежинск',
    site: 'https://snz.rosatom.city/',
    region: 'Челябинская область'
  },
  {
    id: 11,
    city: 'Трёхгорный',
    site: 'https://trg.rosatom.city/',
    region: 'Челябинская область'
  },
  {
    id: 12,
    city: 'Зеленогорск',
    site: 'https://zel.rosatom.city/',
    region: 'Красноярский край'
  }
]
export default {
  data() {
    return {
      slides: DATA,
      swiperOption: {
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        },
        //
        loop: true,
        slidesPerView: 7,
        spaceBetween: 50,
        autoplay: {
          delay: 2500,
          disableOnInteraction: true
        },
        breakpoints: {
          1680: {
            slidesPerView: 7,
            spaceBetween: 50
          },

          1400: {
            slidesPerView: 6,
            spaceBetween: 50
          },
          1080: {
            slidesPerView: 5,
            spaceBetween: 50
          },

          960: {
            slidesPerView: 4,
            spaceBetween: 50
          },

          640: {
            slidesPerView: 3,
            spaceBetween: 50
          },
          320: {
            slidesPerView: 2,
            spaceBetween: 10
          }
        }
      }
    }
  }
}
</script>

<style lang="stylus" scoped>

.swiper
  // &-container
  //   padding-bottom: 4em;


  &-button-next,
  &-button-prev
    position: absolute;
    width 50px
    height 50px
    background #000

  &-pagination-bullets
    width: auto //!important




.Cities

  background #244891
  color #FFF

.city
  &_item
    margin-top 60px
    position relative
    background #FFF
    padding 70px 0 2em
    width 220px
  &_logo
    width 100px
    // height 100px
    position absolute
    top -50px
    left 50%
    transform translateX(-50%)
</style>
