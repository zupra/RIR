<template lang="pug">
  .Page
    Intro
    .wrap
      .subIntro
        // Сколько вовлечено в проект
        InProject
        // География
        Geography
      //- Возможности
      Capatibilities
      .BR
      //- Базовые модули
      BaseModules
      .BR
      //- Дополнительные модули
      .BR
      AdditionalModules
    .BR
    .BR
    //- Города-участники
    Cities
    .BR
    .wrap
      // Разработчики
      Developers
      .BR
      // Новости
      News
      .BR
    // Форма обратной связи
    Form
    // Подвал
    Footer
</template>

<script>
import Intro from '~/components/Intro.vue'
import Cities from '~/components/Cities.vue'
import Form from '~/components/Form.vue'
import Footer from '~/components/Footer.vue'
import BaseModules from '~/components/BaseModules.vue'
import AdditionalModules from '~/components/AdditionalModules.vue'
import Capatibilities from '~/components/Capatibilities.vue'
import Developers from '~/components/Developers.vue'
import News from '~/components/News.vue'
import Geography from '~/components/Geography.vue'
import InProject from '~/components/InProject.vue'

export default {
  components: {
    Intro,
    Cities,
    Form,
    Footer,
    BaseModules,
    AdditionalModules,
    Capatibilities,
    Developers,
    News,
    Geography,
    InProject
  }
}
</script>

<style lang="stylus">
.subIntro
  line-height 1
  h2
    font-size 80px
  .num
    font-size 160px
    color: #1A3670;
    font-weight 800
  .num_bg
    background url("~static/icon/group.png") no-repeat 160px center
h2
  margin-bottom .7em
.BR
  height 4rem
.Page
  //background: url("~static/img/ball.png") no-repeat right 100vh/800px;
  background: url("~static/img/ball.png") no-repeat right 100vh/44vw
  // url("~static/img/ball_2.png")  no-repeat 90% 120vh/50vh;

.Card
  shadow()
  border-radius 5px
  transition 0.3s
  background #FFF
  &:hover
    transform: translate(0, -6px);






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
