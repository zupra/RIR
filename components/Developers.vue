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
    swiper.swiper(
      :options="swiperOption"
    )
      swiper-slide(
        v-for="It in slides"
        :key="It.id"
      ) 
        a.Item.flex.y_center(
          :href="It.link"
          target="_blank"
          :title="It.title"
        )
          .grid
            .H.text_x1.mb-3 {{It.title}}
            p.OVERFLOW {{It.description}}
            //- a.link.mt-3(
            //-     :href="It.link"
            //-     :title="It.title"
            //-     target="_blank"
            //-   ) Смотреть проект
          //- кружок
          .Disc
          picture
            img(
              :src="require(`~/static/img/projects/${It.id}.png`)"
            )

      .swiper-pagination(
        slot="pagination"
      )
      //- .swiper-button-prev(
      //-   slot="button-prev"
      //- )
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
    title: '«Бережливый умный город»',
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
        autoplay: {
          delay: 2500
          // disableOnInteraction: false
        },
        navigation: {
          nextEl: '.swiper-button-next'
          // prevEl: '.swiper-button-prev'
        },
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        },

        breakpoints: {
          1024: {
            slidesPerView: 3,
            spaceBetween: 20
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
  text-decoration none
  color inherit
  border-radius 12px
  //

  position: relative;
  // z-index 2
  overflow: hidden;
  transform: translate3d(0, 0, 0);
  shadow()
  background #FFF
  height 242px
  // ripple()

  picture
    position relative
    z-index 3
  img
    display inline-block
    // right 0
    // height 100%
    // background red

  // transition color .5s, transform 0.5s
  transition color .5s, transform 0.5s

  &:hover
    // mix-blend-mode difference
    // filter: invert(1);
    // backdrop-filter: invert(1)
    // transform scale(1.02)
    // border-radius: 1em;
    transform: translate(0, -4px);
    //box-shadow: 0 3px 5px -1px rgba(0,0,0,.2), 0 6px 10px rgba(0,0,0,.14), 0 1px 18px rgba(0,0,0,.12);







    *
      color #FFF
    .Disc
      opacity 1
      transform: scale(60, 60);

.Disc
  circle(1em)
  background #3889F5
  opacity 0
  position absolute
  z-index 1
  // top 99%
  bottom 2px
  left 2px
  transition: transform 0.75s
  // mix-blend-mode difference
  // filter: invert(1)
  // backdrop-filter: invert(1)


.OVERFLOW
  height 120px
  overflow hidden
.grid
  z-index 2
  padding .9em 0 1em 1.2em
  // padding-right 0
  display: grid;
  // height 392px
  // overflow hidden
  // grid-gap: 10px;
  // grid-template-columns: 1fr 1fr;
  grid-template-rows: 64px 110px 1fr;




.swiper
  margin 0 -8px
  padding 4px
  &-container
    padding-bottom: 4em;
  /*
  &-button-next, &-button-prev
    // position: absolute;
    outline 0
    top auto
    bottom: 0
   &-button-prev
     left 3em
   &-button-next
     right 3em
  */


  &-button-next, &-button-prev
    outline 0
    // top 1.5em;
    height 260px //calc(100% - 4em)
    top 1em
    width 100px
    cursor none
    &:hover
      &:after
        box-shadow: 0 3px 5px -1px rgba(0,0,0,.2), 0 5px 8px rgba(0,0,0,.14), 0 1px 14px rgba(0,0,0,.12);
    &:after
      cursor pointer
      content: '';
      circle(50px);
      background #FFF
      box-shadow: 0px 1px 2px rgba(0, 0, 0, 0.18), 0px 1px 2px rgba(0, 0, 0, 0.04), 0px 2px 6px rgba(0, 0, 0, 0.04);

  &-button-prev
    left 0
    background: linear-gradient(90deg, rgba(#000, 0.3) 0%, rgba(#000, 0.0001) 99%);
    &:after
      background: #FFF url('~static/icon/L.png') no-repeat center;
  &-button-next
    right: 0
    background: linear-gradient(90deg, rgba(#F7F7F7, 0.0001) 0%, rgba(#F7F7F7, 0.7) 99%);
    &:after
      background: #FFF url('~static/icon/R.png') no-repeat center;
</style>
