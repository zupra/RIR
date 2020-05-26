<template lang="pug">
section
  h2.H.text_x5 Разработчики
  .flex.y_center
    .text_x1 АО «Русатом Инфраструктурные решения» — компания-интегратор решений Росатома для создания комфортной жизни в городе.
    a.btn(
      href="https://rusatom-utilities.ru/smart/smart-city.php"
      target="_blank"
    ) Перейти на сайт компании     

  .BR
  client-only
    swiper(
      :options="swiperOption"
    )
      swiper-slide(
        v-for="It in slides"
        :key="It.id"
      ) 
        .Item.flex.y_center
          .grid
            .H.text_x1.mb-3 {{It.title}}
            p.OVERFLOW {{It.description}}
            a.link.mt-3(
                :href="It.link"
                target="_blank"
              ) Смотреть проект
          picture
            img(
              :src="require(`~/static/img/projects/${It.id}.png`)"
            )

      .swiper-pagination(
        slot="pagination"
      )
      .swiper-button-prev(
        slot="button-prev"
      )
      .swiper-button-next(
        slot="button-next"
      )

</template>
<script>
const DATA = [
  {
    id: 1,
    title: 'Платформа «Умный город»',
    description:
      'Позволяет эффективно управлять городским хозяйством, предоставляет новые возможности администрации, бизнесу и жителям города или региона.',
    link: 'https://rusatom-utilities.ru/smart/smart-city-base.php'
  },
  {
    id: 2,
    title: 'LEAN SMART CITY® / «Бережливый умный город»',
    description:
      'Технология непрерывного улучшения системы управления городом. Анализируем, выявляем потери, выстраиваем процессы оптимально, результаты закрепляем в цифровых сервисах.',
    link: 'https://rusatom-utilities.ru/smart/smart-city-lsc.php'
  },
  {
    id: 3,
    title: 'Активный горожанин.',
    description:
      'Цифровой сервис по вовлечению жителей города или всего региона в решение вопросов городского развития.',
    link: 'https://rusatom-utilities.ru/smart/smart-city-ag.php'
  },
  {
    id: 4,
    title: 'Цифровые туристские сервисы',
    description:
      'Гиды-путеводители на городских панелях и в смартфоне, чтобы исследовать город, выбирать интересное в афише мероприятий.',
    link: 'https://fe26.ru/'
  },
  {
    id: 5,
    title: 'Цифровые решения для ЖКХ.',
    description:
      'Проекты по управлению, модернизации и обслуживанию городских систем ресурсоснабжения с применением цифровых технологий.',
    link: 'https://rusatom-utilities.ru/smart/smart-city-gkh.php'
  }
]
export default {
  data() {
    return {
      slides: DATA,
      swiperOption: {
        //
        loop: true,
        slidesPerView: 4,
        spaceBetween: 40,
        // autoplay: {
        //   delay: 2500,
        //   disableOnInteraction: false
        // },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        },
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        },

        breakpoints: {
          1024: {
            slidesPerView: 3,
            spaceBetween: 40
          },
          768: {
            slidesPerView: 2,
            spaceBetween: 50
          },
          640: {
            slidesPerView: 2,
            spaceBetween: 50
          }
          // 320: {
          //   slidesPerView: 1,
          //   spaceBetween: 10
          // }
        }
      }
    }
  }
}
</script>

<style lang="stylus" scoped>


 .Item
  shadow()
  background #FFF
  height 250px
  img
    display block
.grid
  padding 1em
  padding-right 0
  display: grid;
  // grid-gap: 10px;
  // grid-template-columns: 1fr 1fr;
  grid-template-rows: 4em 120px 1fr;

.OVERFLOW
  height 120px
  overflow hidden



.swiper
  &-container
    padding-bottom: 4em;
  &-button-next, &-button-prev
    // position: absolute;
    outline 0
    top auto
    bottom: 0
   &-button-prev
     left 3em
   &-button-next
     right 3em
</style>
