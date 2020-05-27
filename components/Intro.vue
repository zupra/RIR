<template lang="pug">
.Intro
  .topLine
    .wrap
      .upper.flex.x_sb.y_center
        .flex.y_center
          img(
            src="~static/icon/LOGO.png"
          )
          .ml-3 умные города
            br
            | Росатома
        .bold
          nuxt-link(
            :to="{ path: '/', hash:'#About'}"
          ) О проекте
          nuxt-link.mx-5(
            :to="{ path: '/', hash:'#Capabilities'}"
          ) Возможности
          nuxt-link(
            :to="{ path: '/', hash:'#Form'}"
          ) Подать заявку

      .center
        img(
          src="~static/icon/atom.svg"
        )

   
  client-only
    swiper(
      class="swiper"
      :options="swiperOption"
    )
      swiper-slide.wrap(
      ) 
        .flex_wr.x_sb.y_center
          div
            .bold.text_x2.upper.mb-3 Разработчик 
            h1 Русатом 
              br
              | Инфраструктурные 
              br
              | решения
            p.my-4.text_x2 Дивизион Госкорпорации “Росатом” - 
              br
              | интегратор по направлению “Умный город”
            .btn.my-5 Узнать больше о решении
          //
          IntroOl_1
 
      swiper-slide.wrap(
      ) 
        .flex_wr.x_sb.y_center
          div
            h1 Цифровая 
              br
              | платформа 
              br
              | ”Умный город” 
            p.my-4.text_x2 Открытая онлайн-платформа для
              br
              | взаимодействия власти и жителей 
            .btn.my-5 Узнать больше о решении
          //
          IntroOl_2
      

   
      swiper-slide.wrap(
      ) 
        .flex_wr.x_sb.y_center
          div
            .bold.text_x2.upper.mb-3 РЕШЕНИЕ 
            h1 Умные города 
              br
              | Росатома 
            p.my-4.text_x2 Объединяет «атомные» города 
              br
              | на пути цифрового развития
            .flex
              .btn_lite Для жителей
              .btn_lite.mx-3 Для бизнеса
              .btn_lite Для города 
            .btn.my-5 Узнать больше о решении

          //- IntroOl_3
          .flex
            .m_auto.m-3.text_x4 ШАРИКИ ?
      
      
      
      .swiper-pagination(
        slot="pagination"
      )

</template>

<script>
import IntroOl_1 from '~/components/IntroOl_1.vue'
import IntroOl_2 from '~/components/IntroOl_2.vue'
// import IntroOl_3 from '~/components/IntroOl_3.vue'
export default {
  components: {
    IntroOl_1,
    IntroOl_2
    // IntroOl_3
  },
  data() {
    return {
      swiperOption: {
        // effect: 'fade',
        // loop: true,
        direction: 'vertical',
        // autoplay: {
        //   delay: 3000,
        //   disableOnInteraction: false
        // },
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
          dynamicBullets: true
        }
      }
    }
  }
}
</script>

<style lang="stylus" scoped>

.swiper
  height 600px //calc(100% - 160px)

  &-pagination-bullet
    // opacity: initial;
    // background rgba(#FFF, .3) !important
    background: #FFF;
  &-pagination-bullet-active
    background #FFF
  // &-pagination-bullet-active-main


.Intro
  background: #13264D url("~static/img/bg_footer.png") no-repeat center/cover;
  min-height 100vh
  color #FFF
  padding 200px 1em 1em
  position relative

  a
    color #FFF
    text-decoration none



.topLine
  position absolute
  top 1em
  left 1em
  right 1em
  // width 100%




.Grid
  // min-height 100vh
  // grid-gap: 10px;
  display: grid;
  grid-template-rows: 1fr 1fr;


h1
  font-size 60px
</style>
