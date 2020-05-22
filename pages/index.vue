<template lang="pug">
div.Page

  Intro

  .wrap

    .subIntro

      .BR
      h2.H В проекте !!!
        br 
        | участвуют

      .num 880
      .text_x3 тысяч жителей вовлечены
        br
        | в улучшение городской среды

      .num 12
      .text_x3 атомградов используют 
        br
        | умные цифровые сервисы 

      .BR
      .BR
      .BR

      br


      h2.H География
      .MAP
        .num 12
        .text_x3 АТОМНЫХ ГОРОДОВ
        div
          .pulse
          .pulse
          .pulse
          .pulse
          .pulse
          .pulse  
        Slides

        img.MAP_img.img_w(
          src="~static/img/map.png"
        )

    .capabilities
      .center
        h1 Возможности
        p.mt-3 Базовая платформа «Умный город» —  единая информационная основа для внедрения цифровых городских сервисов. Технологии «Умного города» повышают эффективность управления городскими процессами, облегчая жизнь и горожанам, и властям, расширяя возможность обратной связи.
      .BR

      .flex_wr.x_sb
        div
          h3.H Для жителей
          ul
            li Сообщайте о городских проблемах
            li Отслеживайте работу городских служб
            li Узнавайте о работе муниципальных,
              br
              | образовательных и культурных учреждений

        div
          h3.H Для муниципалитетов
          ul
            li Настройте диалог между жителями и властью
            li Улучшайте процессы взаимодействия с жителями
            li Повышайте эффективность работы городских служб


    .BR
    //- Базовые модули
    h2.H  Базовые модули

    .baseModules.mt-5
      .Card.p-3.bg_1

        .flex.x_sb
          h3 Городские 
            br
            | проблемы
          .icon
        .mt-3 Собирает обращения жителей по решению городских проблем, будь то залатать яму, отремонтировать детскую площадку, убрать свалку или пожаловаться на незаконную стройку. Отслеживайте все этапы решения обнаруженной проблемы городскими службами
      .Card.p-3.bg_2
        .flex.x_sb
          h3 Полиция
          .icon
        .mt-3 Показывает границы полицейских участков и контакты участковых. Узнайте, за каким полицейским участком закреплен ваш дом, и обращайтесь к своему участковому.
      .Card.p-3.bg_3
        .flex.x_sb
          h3 Депутатские 
            br
            | округа
          .icon
        .mt-3 Визуализирует границы депутатских округов с контактами депутатов. Депутаты могут отслеживать, с какими проблемами обращаются жители его округа, и участвовать в их быстром решении
      .Card.p-3.bg_4
        .flex.x_sb
          h3 Учреждения
          .icon
        .mt-3 Предоставляет информацию обо всех государственных и муниципальных организациях, образовательных и культурных учреждениях: адреса, графики работы, интернет-ресурсы. Все это есть на нашей платформе


    .BR

  



    //- Дополнительные модули
    h2.H Дополнительные модули
    .text_x1 Платформа «Умный город Росатома» позволяет объединить все муниципальные сервисы. Поключайте дополнительные модули или интегрируйте ваши готовые решения с возможностью их адаптации на платформе.


    .BR
    .additionalModules
  
      .Card.p-3
        .flex.x_sb
          h3.H Общественный транспорт
          .icon
        .Tag Some tag
        p Узнавайте, когда приедет нужный автобус в режиме реального времени. Планируйте свои поездки по городу
      
      .Card.p-3
        .flex.x_sb
          h3.H Уборка улиц
          .icon
        .Tag Some tag
        p Узнайте заранее график уборки улиц, выбирайте маршрут объезда и удобное место парковки, чтобы не помешать спецтехнике.

      .Card.p-3
        .flex.x_sb
          h3.H Оплата услуг
          .icon
        .Tag Some tag
        p Оплачивайте спортивные абонементы, школьное питание и другие городские услуги в одном месте.
      
      .Card.p-3
        .flex.x_sb
          h3.H Достопримечательности
          .icon
        .Tag Some tag
        p Достопримечательности, туристические места, культурные объекты и график их работы. Планируйте свой досуг.

      .Card.p-3
        .flex.x_sb
          h3.H Поликлиники и больницы
          .icon
        .Tag Some tag
        p Найдите ближайшую клинику, узнайте график её работы и запишитесь на приём, не выходя из дома.

      .Card.p-3
        .flex.x_sb
          h3.H Площади в аренду
          .icon
        .Tag Some tag
        p Поможет предпринимателям узнать, где в городе выгодно арендовать подходящее помещение.


  .BR
  .BR
  Cities
  .BR

  .wrap
    h2.H Разработчики
    .flex.y_center
      .text_x1 АО «Русатом Инфраструктурные решения» — компания-интегратор решений Росатома для создания комфортной жизни в городе.
      .btn Перейти на сайт компании

    .scrollList.p-2
      .Card.p-4(
        v-for="_,idx in Array(12)"
      )
        .text_x1.mb-3 Проект Платформа «Умный город»
        p Veniam, id minima sequi nulla, adipisci ullam repudiandae esse iste deleniti eius eveniet? Maiores fugit delectus provident quos sequi veritatis dolor eligendi!

        .bold.mt-3(
          style="color: #2D71F7;"
        ) Смотреть проект
    
    .BR

    h2.H Новости проекта
    .scrollList
      div(
        v-for="_,idx in Array(12)"
      )
        img(
          :src="`https://picsum.photos/id/${idx+10}/300/200`"
        )
        .flex.y_center
          img(
            src="https://icongr.am/octicons/calendar.svg?size=24"
          )
          | &emsp;
          span 30 июл. 2020
        .H.my-2 Lorem ipsum dolor sit amet
        p Приглашаем Вас поделиться мнением и принять участие в «Опросе о работе общественного транспорта в Нижегородской области» … 
    .BR

  Form


  Footer


</template>

<script>
import Intro from '~/components/Intro.vue'
import Cities from '~/components/Cities.vue'
import Form from '~/components/Form.vue'
import Footer from '~/components/Footer.vue'
import Slides from '~/components/Slides.vue'

export default {
  components: {
    Intro,
    Cities,
    Form,
    Footer,
    Slides
  }
}
</script>

<style lang="stylus">



.additionalModules
  display: grid;
  grid-gap: 2em;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr) ) ;
  .icon
    background #CCC
  .Tag
    color: #FFF;
    border-radius: 5px;
    font-weight: 800;
    display: inline-block;

    background: $blue_l;
    padding .3em .7em
    margin-bottom 1em


h2
  margin-bottom .7em

.BR
  height 4rem





.Page
  //background: url("~static/img/ball.png") no-repeat right 100vh/800px;
  background: url("~static/img/ball.png") no-repeat right 100vh/44vw, url("~static/img/ball_2.png")  no-repeat 90% 120vh/50vh;




// .shadow
//   shadow()


.Card
  shadow()
  border-radius 5px
  transition 0.3s
  background #FFF
  &:hover
    transform: translate(0, -6px);



.subIntro
  line-height 1
  h2
    font-size 80px
  .num
    font-size 160px
    color: #1A3670;
    font-weight 800

.capabilities
  .center
    max-width 750px
    margin 0 auto
    line-height 1.6
    font-size 1.2em
  h1
    color: $blue_l
    font-size: 80px;

  li
    padding-left 2.1em
    margin 1em 0
    list-style none
    position relative

    &:before
      position absolute
      left 0
      content ''
      circle(1em)
      background $blue_l



.baseModules
  color #FFF

  display: grid;
  grid-gap: 2em;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr) ) ;


  .bg_1
    background: linear-gradient(52.38deg, #2D71F7 0%, #72CDFF 96.19%);

  .bg_2
    background: linear-gradient(219.74deg, #0266B0 0%, #01468D 85.91%);

  .bg_3
    background: linear-gradient(52.38deg, #54C167 0%, #72CDFF 96.19%);

  .bg_4
    background: linear-gradient(52.38deg, #2D71F7 0%, #CE94F8 96.19%);









.scrollList
  margin 2em 0
  display: grid;
  grid-gap: 2em ;
  grid-template-columns: 1em;
  grid-template-rows: minmax(8rem, 1fr);
  grid-auto-flow: column;
  grid-auto-columns: 310px;

  overflow-x: scroll;
  scroll-snap-type: x proximity;
  scroll-snap-points-x: repeat(100%);
  scroll-snap-type: mandatory;
  scroll-snap-destination: 100% 0%;
  -webkit-overflow-scrolling: touch;
  &::-webkit-scrollbar
     display: none;
  &:before
  &:after
    content: '';
    width: 1em;
</style>
