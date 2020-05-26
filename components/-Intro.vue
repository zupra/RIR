<template lang="pug">
.Intro
  .wrap.Grid
    div
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


    .flex_wr.x_sb.y_center
      div
        h1 Русатом 
          br
          | Инфраструктурные 
          br
          | решения

        p.my-4.text_x2 Дивизион Госкорпорации “Росатом” - 
          br
          | интегратор по направлению “Умный город”


        .flex
          .btn_lite Для жителей
          .btn_lite.mx-3 Для бизнеса
          .btn_lite Для города

        .btn.my-5 Узнать больше о решении

      
      div
        .flex.y_center.mb-4
          img(
            src="~static/icon/logo_2.png"
          )
          .ml-2.text_x5 РОСАТОМ
        ol
          li Ключевой участник национального 
            br 
            | проекта «Цифровая экономика»
          li Участвует в разработке международного
            br 
            | стандарта устойчивого развития малых 
            br 
            | и средних городов
            
          li Создаёт уникальные технологические 
            br 
            | решения на базе перспективных разработкок
            br 
            | атомной отрасли

</template>

<style lang="stylus" scoped>





.Intro
  background: #13264D url("~static/img/bg_footer.png") no-repeat center/cover;
  // min-height 100vh
  color #FFF
  padding 1em

  a
    color #FFF
    text-decoration none

.Grid
  min-height 100vh
  display: grid;
  grid-gap: 10px;
  grid-template-rows: 160px 1fr;


h1
  font-size 60px

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
