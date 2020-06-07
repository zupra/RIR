<template lang="pug">
.Intro
  .topLine
    .wrap
      .upper.flex.x_sb.y_center
        .flex.y_center(
          v-scroll-to="'#Form'"
        )
          img(
            src="~static/icon/LOGO.png"
          )
          .ml-3 умные города
            br
            | Росатома
        div
          b.scrollTo(
            v-scroll-to="'#Cities'"
          ) Города
          b.scrollTo.mx-5(
            v-scroll-to="'#Capabilities'"
          ) Возможности
          b.scrollTo(
            v-scroll-to="'#Form'"
          ) Подать заявку

          //-
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
    swiper.swiper(
      :options="swiperOption"
    )
      swiper-slide.bg_1(
      ) 
        //- .flex_wr.x_sb.y_center
        .wrap.Grid
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
            .btn.my-5(
              v-scroll-to="'#About'"
            ) Узнать больше о решении
          //
          IntroOl_1(
            style="margin-right: -4em"
          )
 
      swiper-slide(
      ) 
        //- .flex_wr.x_sb.y_center
        .wrap.Grid
          div
            h1 Цифровая 
              br
              | платформа 
              br
              | ”Умный город” 
            p.my-4.text_x2 Открытая онлайн-платформа для
              br
              | взаимодействия власти и жителей 
            .btn.my-5(
              v-scroll-to="'#About'"
            ) Узнать больше о решении
          //
          IntroOl_2
      

   
      swiper-slide(
      ) 
        //- .flex.x_sb.y_center
        .wrap.Grid
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
            .btn.my-5(
              v-scroll-to="'#About'"
            ) Узнать больше о решении

          //- IntroOl_3
          .flex
            //- .m_auto.m-3.text_x4 ШАРИКИ ?
            .m_auto.flex.y_center
              .BALL.BALL_1.flex
                img.m_auto(
                  width="320px"
                  src="~static/icon/gifs/2.gif"
                )
                //- Lottie.m_auto(
                //-   :data="animation_2"
                //-   :height="350"
                //-   :width="350"
                //- )
              .flex_col.x_sa
                .BALL.BALL_2
                br
                .BALL.BALL_3.flex
                  img.m_auto(
                    width="260px"
                    src="~static/icon/gifs/5.gif"
                  )
                  //- Lottie.m_auto(
                  //-   renderer="canvas"
                  //-   :data="animation_5"
                  //-   :height="240"
                  //-   :width="240"
                  //- )
      
      
      
      .swiper-pagination(
        slot="pagination"
      )

</template>

<script>
import Lottie from '~/components/Lottie.vue'
import animation_2 from '~/static/animations/JSON/2.json'
import animation_5 from '~/static/animations/JSON/5.json'
//
import IntroOl_1 from '~/components/IntroOl_1.vue'
import IntroOl_2 from '~/components/IntroOl_2.vue'

export default {
  components: {
    Lottie,
    IntroOl_1,
    IntroOl_2
    // IntroOl_3
  },
  data() {
    return {
      animation_2,
      animation_5,
      swiperOption: {
        effect: 'fade',
        // speed: 2500,
        // loop: false,
        mousewheel: true,
        direction: 'vertical',
        freeModeSticky: true,
        freeMode: true,
        resistance: false,

        autoplay: {
          delay: 5000
          // stopOnLastSlide: true
          // disableOnInteraction: false
        },
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
          dynamicBullets: true
          // bulletClass: 'bullet',
          // bulletActiveClass: 'bullet-active'
          // type: 'fraction'
        }
      }
    }
  }
}
</script>

<style lang="stylus">
.Intro
  .swiper-pagination
    &-bullets
      width 20px !important
    &-bullet
      width 18px !important
      height 18px !important
      // margin: 10px 0 !important
      background #FFF !important
      // &-active

  ol
    counter-reset: counter_li;

  li
    height 5em
    font-weight bold
    font-size 1.2em


    list-style none
    padding-left 108px
    position relative


    &:before
      position absolute
      left 8px
      // content ''
      color $blue_l
      counter-increment: counter_li;
      content: "0" counter(counter_li);
      font-weight 800
      font-size 1.4rem

      circle(3em)
      line-height 3em
      text-align center

      background #FFF
</style>

<style lang="stylus" scoped>


.scrollTo
  cursor pointer


.BALL
  background #FFF
  &_1
    circle(400px)
    // background  #FFF url("~static/icon/gifs/2.gif") center no-repeat
  &_2
    circle(250px)
    background  #FFF url("~static/icon/ball_atom.svg") center no-repeat
  &_3
    circle(300px)
    // background  #FFF url("~static/icon/gifs/5.gif") center no-repeat




.swiper
  height 100vh //600px //calc(100% - 160px)
  // margin-top 7vh
  // &-wrapper
  &-slide
    padding calc(150px + 10vh) 1em 1em
    background url("~static/img/bg_2.png") no-repeat center/cover;
    &.bg_1
      background url("~static/img/bg_1.png") no-repeat center/cover;
  &-slide,
  &-slide-prev
    // visibility: hidden;
    opacity 0
    &-active
      // visibility visible
      opacity 1

  // &-pagination-bullets
  //   width 20px

  // &-pagination-bullet
  //   // opacity: initial;
  //   // background rgba(#FFF, .3) !important
  //   background: #FFF;
  // &-pagination-bullet-active
  //   background #FFF
  // &-pagination-bullet-active-main


.Intro
  background: #13264D // url("~static/img/bg_1.png") no-repeat center/cover;
  min-height 100vh
  color #FFF
  // padding 200px 1em 1em
  position relative
  a
    color #FFF
    text-decoration none

.topLine
  position absolute
  top 1em
  left 1em
  right 1em
  z-index 10
  // width 100%




.Grid
  // min-height 100vh
  // grid-gap: 10px;
  display: grid;
  grid-template-columns: 4fr 3fr;

h1
  font-size 60px
</style>
